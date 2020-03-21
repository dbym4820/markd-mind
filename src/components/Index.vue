<template>
    <b-container class="text-center" fluid>
	<b-row><b-col><HeaderMenu /></b-col></b-row>
	<b-row class="mainField">
	    <b-col cols="1" class="fileArea rounded"><FolderList /></b-col>
	    <b-col cols="6" class="editorArea rounded"><Editor /></b-col>
	    <b-col class="mermaidArea rounded"><MermaidEditor /></b-col>
	</b-row>
	<b-row><b-col><FooterMenu /></b-col></b-row>
    </b-container>
</template>

<script>
 import HeaderMenu from './Menu/HeaderMenu'
 import FooterMenu from './Menu/FooterMenu'
 import FolderList from './Index/FolderList'
 import FilterableDropdown from './Index/FilterableDropdown'
 import Editor from './Index/Editor'
 import MermaidEditor from './Index/MermaidEditor'
 export default {
     name: 'Index',

     components: {
	 HeaderMenu, FooterMenu,
	 FolderList,
	 FilterableDropdown,
	 Editor,
	 MermaidEditor,
     },
 }
</script>

<style>
 body {
     background-color: #343A40;
 }
 .mainField {
     height: 100%;
 }
 .filterArea {
     background-color: yellow;
 }
 .mermaidArea {
     background-color: black;
 }

</style>
