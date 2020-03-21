<template>
    <div class="editor-container text-left rounded">
	<b-tabs content-class="pills">
	    <b-tab v-for="file in files"
		   v-bind:title="file.title"
		   v-bind:key="file.id">
		<MDItem></MDItem>
	    </b-tab>
	</b-tabs>
    </div>
</template>

<script>
 import MDItem from './Editor/MDItem' 
 export default {
     name: 'Editor',
     components: {
	 MDItem,
     },
     method: {
	 
     },
     data() {
	 return {
	     current: "init",
	     files: [
		 { id : "1", title : "tab1", content : "sam1" },
		 { id : "2", title : "tab2", content : "sam2" },
		 { id : "3", title : "tab3", content : "sam3" },
	     ],
	 }
     },

 }
</script>

<style>
 .editor-container {
     background-color: #93a0ad;
 }
</style>
