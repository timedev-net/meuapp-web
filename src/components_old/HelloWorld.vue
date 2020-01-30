<template>
  <div>
    <h1>{{ msg }}</h1>
    <ul v-for="data in dados" :key="data">
      <li>
<!--          <img :src="'teste'+data.arquivo_foto" alt="foto" width=60 height=40>-->
          <img src="https://conexaofreelancer.com.br/wp-content/uploads/2018/06/Pessoa.png" alt="foto" width=60 height=60><br>
<!--          {{ data.arquivo_foto }}-->
          {{ data }}
      </li>
    </ul>
    <ul>
      <li>
<!--        {{ dados.apenados.data[0].nomeapenado }}-->
      </li>
    </ul>
    
  </div>
</template>

<script>
export default {
  data() {
		return {
      dados: []
		}
	},
  name: 'HelloWorld',
  props: {
    msg: String
  },
  // methods: {
  //   obterUsuarios() {
	// 		this.$http.get('semtoken/foragidos').then(res => {
	// 			this.dados = res.data
	// 			//console.log(res.data)
	// 		})
	// 	}
  // },
  created() {
    // this.$http.post('authenticate').then(res => {
    //
    // })

    this.$http.get('').then(res => {
				this.dados = res.data
        /*eslint-disable */
				console.log(res.data) // eslint-disable-line no-use-before-define
        /*eslint-enable */
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
