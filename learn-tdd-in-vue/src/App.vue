 <template>
   <div>
    <new-message-form @send="addMessage" />
   </div>
 </template>

 <script>
import NewMessageForm from './components/NewMessageForm';
import MessageList from './components/MessageList';
 export default {
   name: 'App',
   components: {
    NewMessageForm,
  },
  data() {
    return {
      messages: [],
    };
  },
  methods: {
    addMessage(text) {
      this.messages.unshift(text);
    },
  },
 };
 </script>
