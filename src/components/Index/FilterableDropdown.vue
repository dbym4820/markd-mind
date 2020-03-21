<template>
    <div ref="wrapper" class="fd__wrapper">
    </div>
</template>

<script>
 export default {
     name: 'FilterableDropdown',
     data() {
	 return {
	     filterString: null,
	     showList: false
	 };
     }
 }
</script>
