# Resizing the ACE Editor 

It's not enough to simply change the CSS values in an ACE editor in order to resize it, you must also call the [`resize`](https://github.com/josdejong/jsoneditor/issues/131#issuecomment-55874095) function after you have changed the CSS dimensions.

Here is a snippet from [Livewire](https://github.com/Infragistics/livewire):

````
showResults: function(){              
    $editor.css('width', appSettings.editorWidth());
    editor.resize();    
},

hideResults: function(){    
    $editor.css('width', ($window.width() - appSettings.resultsButtonWidth() + 1) + 'px');
    editor.resize();    
}
````