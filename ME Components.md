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
|Name Of Prop| Detail|Type |Values
-------------|-------|--------|-----|
`Style` | Normal inline react css handling.|`Object`| Eg. `{{ height:40}}`
`className`| Predefined css classes |`String` | "som-random-css-class and-another-one"
`onClick` | onClick handler. Provides **`event`** param | `function` | `(event)=> { e.preventDefault() }`
`mediaType`| Specify what kind of media type to be displayed with the button text | `String` | `"icon"` or  `"image"`
`icon` | Media content to be displayed if mediaType is set | `String` or `Blob` | `fa fa-check` or `www.placeholder.com/images/450` or `Imported Image` 
`iconStyle` | Inline styles to modify the way the icon is displayed|`Object` | `{{ color:"green", size:45}}`
`href` or `to` |  Makes the button behave as an anchor link, while maintaining its button look | `String` | `www.massenergize.com` 
`variation` | Switch between three different button designs | `String` | `accent`, `union`, `normal`  *(default = normal)*


