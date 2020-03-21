<template>
    <div>
    </div>
</template>

<script>
 import Vue from 'vue';
 import VueMermaid from "vue-mermaid";
 Vue.use(VueMermaid)
 export default {
     name: 'MermaidEditor',
     data : function(){
	 return {
	     data:[
		 {id:'1',text:'A',link:'---',next:['2'],editable:true},
		 {id:'2',text:'B',edgeType:'circle',next:['3']},
		 {id:'3',text:'C',next:['4','6']},
		 {id:'4',text:'D',link:'-- This is the text ---',next:['5']},
		 {id:'5',text:'E'},
		 {id:'6',text:'F'}
	     ]
	 }
     },
     methods:{
	 editNode(nodeId) {
	     alert(nodeId);
	 },
     }
 }
</script>
