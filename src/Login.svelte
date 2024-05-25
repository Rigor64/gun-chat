<script>
  import { user } from './user';

  let username;
  let password;

  function login() {
    user.auth(username, password, ({ err }) => err && alert(err));
  }

  function signup() {
    user.create(username, password, ({ err }) => {
      if (err) {
        alert(err);
      } else {
        login();
      }
    });
  }
</script>


<input name="username" bind:value={username} minlength="3" maxlength="16" placeholder="Username" />
<input name="password" bind:value={password} type="password" placeholder="Password"/>

<div style="display: flex, align: center ">
<button class="login" on:click={login}>Login</button>
<button class="login"  on:click={signup}>Sign Up</button>
</div>

  
