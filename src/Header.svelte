<script>
  import { username, user } from './user';

  function signout() {
    user.leave();
    username.set('');
  }
</script>

<header>
<h1>🌳</h1>
  {#if $username}
    <div class="user-bio">
      
      <img src={`https://api.dicebear.com/8.x/pixel-art/svg?seed=${$username}`} alt="avatar" /> 
      <span><strong>{$username}</strong></span>
    </div>

    <button class="signout-button" on:click={signout}>Sign Out</button>

    {:else}

      <h2 class="app-name">JogTalk</h2>
  {/if}
</header>