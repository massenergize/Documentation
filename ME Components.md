## CUSTOM M.E COMPONENT DOCUMENTATION 
Below are a few components that have been created to suit MassEnergize's unique needs. All these components are made with pure react and use props. The current props of all these components are subject to change! Work on anything or change any thing to suit your situation as the occassion demands. However, take a look at the various properties before you start editing any components, your needs might already have been implemented! Let's get started :fire:
* <a href="#me-button">MEButton </a>
* <a href="#me-textfield">METextField </a>
* <a href="#me-textview">METextView </a>
* <a href="#me-radio-group">MERadioGroup</a>
* <a href="#me-checkbox-group">MECheckboxGroup</a>
* <a href="#me-file-selector">MEFileSelector</a>
* <a href="#me-form-generator">MEFormGenerator </a>
* <a href="#me-section">MESectionWrapper </a>
* <a href="#me-modal">MEModal </a>
* <a href="#me-chip-maker">MEChipMaker </a>
* <a href="#me-card">MECard </a>
* <a href="#me-dropdown">MEDropdown </a>

NOTE: The below listed properties of each component are easily subject to change. While these docs are updated from time to time, there is a chance that somethings might have changed in  various places. 
### <a name ="me-button">MEBUTTON </a>
Has all the features that the normal button has and accepts all the default props as well. Comes with accepted button styles out of the box, but open to any kind of tweaks via the provided channels below.
|Property| Description |Type |Values Or Examples
-------------|-------|--------|-----|
**`Style`** | Normal inline react css handling.|`Object`| Eg. `{{ height:40}}`
**`className`**| Predefined css classes |`String` | "som-random-css-class and-another-one"
**`onClick`** | onClick handler. Provides **`event`** param | `function` | `(event)=> { e.preventDefault() }`
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
**<span style="color:red">name </span>** | Name of field | `String` | `input_box`
**`placeholder`** | Placeholder text | `String` | `Enter text here...`
