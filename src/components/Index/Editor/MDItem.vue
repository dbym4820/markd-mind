<template>
    <div class="form-group">
	<markdown-editor
	    v-model="value"
	    toolbar="bold italic heading | image link | numlist bullist code quote | preview fullscreen"
	    buttonClass="btn btn-outline-success"
	    height="100%"
	    :options="options">
	</markdown-editor>
    </div>
</template>

<script>
 import 'v-markdown-editor/dist/v-markdown-editor.css'
 import Vue from 'vue'
 import Editor from 'v-markdown-editor'

 Vue.use(Editor)
 export default {
     name: 'Editor',
     components: {
	 Editor,
     },
     methods: {
	 onChangeInput(event) {
	     this.value = event.target.value;
	     this.commitChange(event.target.value)
	 },
	 commitChange(newValue) {
	     this.$emit('input', newValue)
	 },
     },
     data() {
	 return {
	     value: "sample",
	     options: {
                 lineNumbers: true,
		 styleActiveLine: true,
		 styleSelectedText: true,
		 lineWrapping: true,
		 indentWithTabs: true,
		 tabSize: 2,
		 indentUnit: 2
             }
	 }
     },
 }
</script>

<style>
 #editor{
     height: 100%;
 }
 #editor .quill-editor {
     height: 100%;
 }
 #editor .quill-editor .ql-container {
     height: 100%;
 }

 h2 {
     display: block;
     font-size: 1.5em;
     margin-block-start: 0.83em;
     margin-block-end: 0.83em;
     margin-inline-start: 0px;
     margin-inline-end: 0px;
     font-weight: bold;
 }

</style>
