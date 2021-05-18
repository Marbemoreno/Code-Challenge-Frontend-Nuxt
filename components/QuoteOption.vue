<template>
	<div class="cuote-option row justify-content-center" >
		<div class="col-4">{{$props.value.descripcion}}</div>
		<div class="col-4 justify-content-center"> {{costoSubmit}}</div>
		<div class="col-4"> {{$props.value.PlazoEntrega}} </div>
		
	</div>
</template>

<script>
	
export default {
	
	props: {
		value: {
			type: Object,
			required: true
		}
	},
	
	computed:{
	  costoSubmit(){
		return  this.$props.value.Total === 0?'Gratis':this.$props.value.Total
		  },
	}

}

</script>

<style lang="scss" scoped>
.cuote-option{
	padding:6px 10px;
	box-shadow: black;
	background-color: #006FE6;
	color: white;
	text-align: center;
	
	div{
		align-self: center;
	}
	&:first-child{
		background-color: white;
		color: black;
		font-weight: bold;
		border-top-left-radius: 15px;
		border-top-right-radius: 15px;
		border: 2px solid #006FE6;
		font-size: 1.3rem;
		
		border-bottom:0px;
	}
	&:last-child{
		border-bottom-left-radius: 15px;
		border-bottom-right-radius: 15px;
	}
	&:nth-child(2n) {
	background-color: #005CBF;
	color:white
}
}

</style>
