<template>
  <div class="messages">
    <h1 class="text-center">{{ msg }}</h1>

    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="panel panel-default">
            <div class="panel-heading">
              <h4 class="panel-title">Mensagens</h4>
            </div>
            <div class="panel-body">
              <div class="col-md-6">
                <form action="">
                  <div class="form-group">
                    <label for="new-message-user" class="control-label">Usuário</label>
                    <input type="text" id="new-message-user" v-model="newMessage.user" class="form-control">
                  </div>
                  <div class="form-group">
                    <label for="message-text">Mensagem</label>
                    <textarea name="messa-text" id="message-text" v-model="newMessage.text" class="form-control" cols="30" rows="10"></textarea>
                  </div>
                  <div class="form-group">
                    <div class="pull-right">
                      <button type="button" class="btn btn-primary btn-sm" v-bind:disabled="!newMessage.user || !newMessage.text" v-on:click="enviarMensagem(newMessage)">Enviar</button>
                      <button type="button" class="btn btn-danger btn-sm" v-on:click="">Cancelar</button>
                    </div>
                  </div>
                </form>
              </div>
              <div class="col-md-6">
                {{ messages }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>    
  </div>
</template>

<script>
export default {
  name: 'messages',
  data() {
    return {
      msg: 'Vue Js Messages',
      newMessage: {
        user: '',
        text: '',
      },
      messages: [],
    };
  },
  methods: {
    enviarMensagem(message) {
      this.messages.push(message);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
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
