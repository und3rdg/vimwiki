```javascript
  branchesFilterAutoSubmit: function(){
    var container = '.branches__bottom__form'
    var listItem = 'li[data-val]'
    var form = '.branches__bottom__form form'
		if($(container).length){
      $(container).find(listItem).click(function(){
        $(form).submit()
      })
    }
  },
  ```
