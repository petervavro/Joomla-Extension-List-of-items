# Module: List of Items | FILTERS
The module is adding filter functionality, for the main component. Currently there are following options available:

## By category
To display only items within certain category.
```
<field 
    name="categoryid"
    type="customcategory"
    extension="com_listofitems"
    label="JCATEGORY"
    class="form-control"
    order="alphabetical"
    showamount="true"
    rootcategoryid="root"
    onchange="this.form.submit();" />
```
### Attributes
| Name | Description |
| ----------- | ----------- |
| `label` | The descriptive title of the field. |
| `rootcategoryid` | The root category, the parent category of the filter. You can replace "root" value for desired category id. Category id, can be found in the last column of the table at "List Of Items: Categories" view (Component > List of Items > Categories). |

## By arbitrary string
To display items which contains the input string value.
```
<field name="text"
    type="text"
    label="COM_LISTOFITEMS_FIELD_SEARCH_FULLTEXT_LABEL"
    class="form-control"
    placeholder="COM_LISTOFITEMS_FIELD_SEARCH_FULLTEXT_LABEL" />
```
### Attributes
| Name | Description |
| ----------- | ----------- |
| `label` | The descriptive title of the field. |
| `placeholder` | The text displayed in the html placeholder element. |

## By first letter
To display items which first letter in their title match the selected one. For users convenience, it displays first letters of all items in current  category. These letters are displayed each as a button. After user clicks on the button only items with first letter of title matching the selection will be displayed. All "first letter" buttons also serves as submit button for the form.
```
<field name="letter"
    type="filterbyfirstletter"
    label="COM_LISTOFITEMS_FILTER_FIRST_LETTER_LABEL"
    classwrapper="btn-group btn-group-sm d-flex"
    classletter="btn btn-secondary d-flex justify-content-center align-items-center"
    classletteractive="btn btn-primary active disabled d-flex justify-content-center align-items-center"
    classreset="btn btn-outline-secondary d-flex justify-content-center align-items-center" />
```
### Attributes
| Name | Description |
| ----------- | ----------- |
| `label` | The descriptive title of the field. |

## By value in "feature" column
To display items which contains the selected value in particular column. It represents a drop down list input of custom-defined entries, to be selected from. When an user selects an option from the list, only items having the selected value in searched "feature" column will be displayed.
```
<field 
    name="feature_1"
    type="list" 
    default="" 
    label="Select an option">
    <option value="">Please Select</option>
    <option value="A">Option A</option>
    <option value="B">Option B</option>
    ...
</field>
```
The list option must be defined in `<option>` element e.g. `<option value="?">?</option>`

### Attributes
| Name | Description |
| ----------- | ----------- |
| `name` | The id of column to search in for the value. The value ca be only one of these: "feature_1", "feature_2", "feature_3", "feature_4", "feature_5", "feature_6", "feature_7", "feature_8", "feature_9", "feature_10", "feature_11", "feature_12", "feature_13", "feature_14", "feature_15", "feature_15", "feature_17", "feature_18", "feature_19", "feature_20" |
| `label` | The descriptive title of the field. |


## Form definitions
The filter options displayed in form can be selected.
You can choose filters you like to display, by submitting custom form XML definition. You can find input textarea to submit XML is available within module options `"Custom form (XML)"`.

In following lines you can find samples of form definition.

### For template using Bootstrap v2
Customized forms optimized for use with template based on Bootstrap version 2.
* `all_BootstrapV2.xml` : Form with all filters.
* `filter-by-first-letter/BootstrapV2.xml` : Form with "by first letter" filter only.

### For template using Bootstrap v3
Customized forms optimized for use with template based on Bootstrap version 3.
* `all_BootstrapV3.xml` : Form with all filters.
* `filter-by-first-letter/BootstrapV3.xml` : Form with "by first letter" filter only.

### For template using Bootstrap v4
Customized forms optimized for use with template based on Bootstrap version 4.
* `all_BootstrapV4.xml` : Form with all filters.
* `filter-by-first-letter/BootstrapV4.xml` : Form with "by first letter" filter only.