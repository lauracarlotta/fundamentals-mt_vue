<template>
	<div>
		<form @submit="sendForm($event)">
			<!-- <InputText/> -->
			<!-- <InputText/> -->
			<br/>
			<div>
				Apelido: 
				<input type="text" v-model="apelido">
			</div>
			<div>
				Cor Favorita: 
				<input type="text" v-model="corFavorita">
			</div>
			<br/>
			<Submit/>
		</form>
		<ReutilizacaoComponent/>
	</div>
</template>

<script>
	// import InputText from './Form/InputText.vue;'
	import Submit from './Form/Submit.vue';
	import ReutilizacaoComponent from './ReutilizacaoComponent/ReutilizacaoComponent.vue';

	export default {
		name: 'Form',

		components: {
			// InputText,
			Submit,
			ReutilizacaoComponent,
		},

		data() {
			return {
				apelido: "",
				corFavorita: "",
			}
		},

		methods: {
			sendForm(e) {
				e.preventDefault();
				
				const apelido = this.apelido;
				const corFavorita = this.corFavorita;

				console.log('apelido', apelido);
				console.log('cor', corFavorita);

				// AJAX

				// Inserir nop banco, os dados
			}
		}
	}
</script>
