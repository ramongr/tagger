[![Code Climate](https://codeclimate.com/github/ramongr/tagger.png)](https://codeclimate.com/github/ramongr/tagger)
# Tagger
A js tagging lib using [Foundation](foundation.zurb.com) assets

## Flags

### Their default value

Flags marked with * are essencial
- allowDuplicates: true
- buttonId: null *
- filterId: 'tagger-filter' *
- hiddenInputId: null *
- indexableTagList: []
- labelClass: ''
- tagList: null
- onlyTagList: false
- tagCloseIcon: 'X'
- tagContainerId: null *
- tagListContainerId: null *
- tagListContainerHeight: 300 *
- tagListFormat: null
- tagListStart: null

###What do they do

**allowDuplicates**

This flag controls the acceptance of duplicates in the form

**buttonId**

The button that will trigger the dropdown and the input for filtering

Example:
```
$(selector).tagger({
  buttonId: '_someOtherID_'
})
```

**filterId**

The filterId will have two functionalities, first it can filter elements from a given tagList but it will also be able to add non-listed elements using the colon key &#44;

**hiddenInputId**

This hidden input is where your form will get the information from the tags

Example:
```
$(selector).tagger({
  hiddenInputId: '_someID_'
})
```

**indexableTagList**

If a tag has more information than just it's name, then this flags helps to assure tags aren't duplicated or not permitted

**labelClass**

Some extra CSS class you might want to add to your label

Example:
```
$(selector).tagger({
  labelClass: '_someFancyClass_'
})
```

**onlyTagList**

Limits tag insertion to a list

**tagList**

An array of tags

**tagCloseIcon**

Ability to customize the closing symbol in the label

**tagContainerId**

This is where the labels will be printed out

**tagListContainerId**

If you want to show a tag list, then they will show up in a dropdown every time you give focus to the input

**tagListContainerHeight**

This is the default height of the foundation dropdown, adjust it at will, it's defined in pixels

**tagListFormat**

This determines the format of the array you will receive on _tagList_ there are limited options

1. A simple array, then this flag should remain null
Example:
```
$(selector).tagger({
    tagList: ['Apples', 'Oranges'],
    tagListFormat: null
})
```

2. An array of arrays, this usually means you don't want to save the tag name but the tag id
Example:
```
$(selector).tagger({
    tagList: [[1,'Apples'],[2, 'Oranges']],
    tagListFormat: ['id', 'name']
})
```
By using the keywords 'id' and 'name', tagger knows it should display the 'name' to the lib user and the id in the hidden input to be stored somewhere

**tagListStart**

If you want to edit a tag cloud, then it should be able to remember which tags where added before, this option is used for those cases


### Using tagger
1. Minimum configuration :
```
$(selector).tagger({
    buttonId: "_some_button_id_",
    hiddenInputId: "_some_hidden_input_id_",
    tagContainerId: "_some_container_id_",
    tagListContainerId: "_some_container_id_",
})
```
