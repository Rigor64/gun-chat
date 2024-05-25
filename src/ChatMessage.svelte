<script>
  export let message;
  export let sender;

  const messageClass = message.who === sender ? 'sent' : 'received';

  const avatar = `https://api.dicebear.com/8.x/pixel-art/svg?seed=${message.who}`;

  const ts = new Date(message.when);
</script>

<div class={`message ${messageClass}`}>
  <img class="avatar" src={avatar} alt="avatar" />
  <div class="message-text">
    <h3 class="avatar-name">{message.who}</h3>
    <p>{message.what}</p>
    <time>{ts.toLocaleTimeString()}</time>
  </div>
</div>
