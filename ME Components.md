## CUSTOM M.E COMPONENT DOCUMENTATION 
Below are a few components that have been created to suit MassEnergize's unique needs. All these components are made with pure react and use props. The current props of all these components are subject to change! Work on anything or change any thing to suit your situation as the occassion demands. However, take a look at the various properties before you start editing any components, your needs might already have been implemented! Let's get started :fire:
* <a href="#me-button">MEButton </a>
* <a href="#me-textfield">METextField </a>
* <a href="#me-textview">METextView </a>
* <a href="#me-radio-group">MERadioGroup</a>
* <a href="#me-checkbox-group">MECheckboxGroup</a>
* <a href="#me-file-selector">MEFileSelector</a>
* <a href="#me-dropdown">MEDropdown </a>
* <a href="#me-section">MESectionWrapper </a>
* <a href="#me-modal">MEModal </a>
* <a href="#me-chip-maker">MEChipMaker </a>
* <a href="#me-card">MECard </a>
* <a href="#me-form-generator">MEFormGenerator </a>


NOTE: The below listed properties of each component are easily subject to change. While these docs are updated from time to time, there is a chance that somethings might have changed in  various places. 
### <a name ="me-button">MEBUTTON </a>
Has all the features that the normal button has and accepts all the default props as well. Comes with accepted button styles out of the box, but open to any kind of tweaks via the provided channels below.
|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`Style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:40}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`onClick`** | onClick handler. Provides **`event`** param | `function` | `(event)=> { event.preventDefault() }`
**`mediaType`**| Specify what kind of media type to be displayed with the button text | `String` | `"icon"` or  `"image"`
**`icon`** | Media content to be displayed if mediaType is set | `String` or `Blob` | `fa fa-check` or `www.placeholder.com/images/450` or `Imported Image` 
**`iconStyle`** | Inline styles to modify the way the icon is displayed|`Object` | `{{ color:"green", size:45}}`
**`href` or `to`** |  Makes the button behave as an anchor link, while maintaining its button look | `String` | `www.massenergize.com` 
**`variation`** | Switch between three different button designs | `String` | `accent`, `union`, `normal`  *(default = "normal")*

### <a name="me-textfield">METEXTFIELD</a>
Massenergize custom input box. Fields in <span style="color:red">red </span> are compulsory.
|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:30}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`onChange`** | onChange handler. Provides **`event`** param | `function` | `(event)=> { console.log(event.target.value)}`
**`inputType`**| Choose between a normal input or textarea | `String` or  | `input` or `textarea`
**`rows`** |default number of rows if textarea | `String` |  `"12"` 
**`value` or `defaultValue`** | Any of the fields  will work. Used to set the default value of the input *not textarea* <span style="color:red">*(should not be null or undefined)*</span>|`String` | `"Any kind of text"`
**`type`** |  Content type of the input. Normal html input types | `String` | `text` or `password` or `number` etc. 
**`readonly`** | Set field to be readonly | `boolean` | `true` or `false`
**`history`** | Remember previous inputs | `boolean` | `true` or `false`
**`isRequired`** | Set as a compulsory field | `boolean` | `true` or `false`
**<span style="color:red">name (required) </span>** | Name of field | `String` | `input_box`
**`placeholder`** | Placeholder text | `String` | `Enter text here...`
### <a name="me-textview">TEXTVIEW</a>
Custom paragraph component for MassEnergize.   
|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:30}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`onChange`** | onChange handler. Provides **`event`** param | `function` | `(event)=> { console.log(event.target.value)}`
**`type`**| Choose between a normal <p> or <small> tag | `String`  | `p` or `paragraph` or `small`


### <a name="me-radio-group">MERADIOGROUP</a>
A component that takes an array of strings and renders each string as a radio button. On selection, it returns the string value of the selected radio button. Returns null, if unslected. 

|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:30}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`containerClassName`**| Predefined css classes used to style the div that holds all the radio buttons. |`String` | "som-random-css-class and-another-one"
**`containerStyle`**| Normal inline css styles for the container div |`Object` | Eg. `{{ height:30}}`
**`onItemSelected`** | Returns the selected string value of the radio button everytime an item is selected| `function` | `(item)=> { console.log(item)}`
**`data (required)`** |Array of string values| `Array of strings` | `["Home", "House", "Crib"]`
**`dataValues (optional)`** |In the case where a different value should be returned when a radio button is checked, the values should be provided in this field. The `dataValues` field also accepts an an Array that should be the **same size as data** | `Array` | `["ValueForHome", "ValueForHouse","ValueForCrib"]` _**NB: data and dataValues here have the same array length of 3**_


### <a name="me-checkbox-group">MECHECKBOXGROUP</a>
A component that takes an array of strings and renders each string as a checkbox. On selection, it returns the all the checked items, and the currently selected option.  

|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:30}}`
**`fineTuneStyle`** | Normal inline react css handling used to modify the styling of the box design that represents the checkmark.|`Object`| Eg. `{{ color:"lime"}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`containerClassName`**| Predefined css classes used to style the div that holds all the checkboxes. |`String` | "som-random-css-class and-another-one"
**`containerStyle`**| Normal inline css styles for the container div |`Object` | Eg. `{{ height:30}}`
**`onItemSelected`** | Returns all the items that have been selected and the just selected item as different params | `function` | `(allItems, justSelectedItem)=> { console.log(justSelectedItem)}`
**`data (required)`** |Array of string values| `Array of strings` | `["Check1", "Check2", "Check3"]`
**`dataValues (optional)`** |In the case where a different value should be returned when a checkbox is checked, the values should be provided in this field. The `dataValues` field also accepts an an Array that should be the **same size as data** | `Array` | `["ValueForCheck1", "ValueForCheck2","ValueForCheck3"]` _**NB: data and dataValues here have the same array length of 3**_


### <a name="me-file-selector">MEFILESELECTOR</a>
The MEFileSelector is a more polished and advance version of the normal HTML input file selector. It looks much better, it allows users to crop, and it resizes all it's images on the fly.  Available props include: 

|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:30}}`
**`previewStyle`** | Normal inline react css used to modify the image tag that shows a preview of the user's selected image.|`Object`| Eg. `{{ color:"lime"}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`ratioWidth`**| Spcecify aspect ratio width for cropping box |`Number` | Eg. 4
**`ratioHeight`**|Spcecify aspect ratio heigh for cropping box |`Number` | Eg. 3 |
**`onFileSelected (required)`** | Returns a resized **FileObject** of the selected image. If user uses the cropping feature, it returns the cropped version instead with other important related data | `function` | `(data, aResetFunction)=> { console.log(data.croppedFile)}`
**`maxWidth`** |Set the max width value of the cropping box| `Number` | Eg. 500
**`maxHeight`** |Set the max height value of the cropping box| `Number` | Eg. 450
**`name (required)`** |Name of field| `String` | "testibox_img_selector"
**`showOverlay`** |Show a transaparent overlay over screen when in cropping mode| `boolean` | `true or false` *default = true*

**Details on `onFileSelected` parameters**<br/>
The function returns `data`, which is a json object that contains a resized version of the just selected image, the original image, as well as some other size and file name details from the original file <br/>
**NB: When the user uses the cropper on their image, the resized and cropped image  can be accessed from the `croppedFile` field. If the user does not use the cropper, the image still gets resized, but not cropped and is still accessed from the `croppedFile` field**. 
```javascript 
 {
   originalFile: File ...{} // JS file object, 
   originalSize:{ size:223389, text:"223KB"}
   croppedFile: File ...{} // JS file object 
   croppedSize: { size:32989, text:"30KB"}
   originalFileName: "some-random-name-a-user-has-given-to-their-file.jpg"
 }
```
The `OnFileSelected` function also returns a reset function as a second parameter, so that the component can be reset outside of itself.

```javascript
  <MEFileSelector 
  onFileSelected ={(data,reset)=>{
    //....... do this and that 
    //... then clear everything 
    reset(); //... you might want to save this somewhere for last stages.LOL!
  }}>
```

### <a name="me-dropdown">MEDROPDOWN</a>
Need to display a list of items that user will choose from? Try the MEDropdown. 

|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:30}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`onItemSelected`** | Returns the value of the item that has been selected | `function` | `(item)=> { console.log(item)}`
**`data (required)`** |Array of string values| `Array of strings` | `["First list item", "Second list item", "Third list item"]`
**`dataValues (optional)`** |In the case where a different value should be returned when an item is selected, the values should be provided in this field. The `dataValues` field also accepts an an Array that should be the **same size as data** | `Array` | `["Value for item1", "Value for item2","Value for item3"]` _**NB: data and dataValues here have the same array length of 3**_

**More Details** <br/>
```javascript
()=>{
  const data = ["Shoes", "Bags","Shirts"] // items for sale
  const dataValues = [100,450,5] // prices in USD

// If a user selectes Bags from the dropdown GUI
  <MEDropdown 
    data = {data} 
    dataValues={dataValues} 
    onFileSelected={(value)=>{
    console.log(value) // value will be equal to === 450, not "Bags" 
    //value would only be === "Bags" if the dataValues field was not provided
  }}>

}

```