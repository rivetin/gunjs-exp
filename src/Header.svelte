<script>
  import { username, user } from "./user";

  function signout() {
    user.leave();
    username.set("");
  }
</script>

<header>
  <h1>SuperChat v0.2</h1>
  {#if $username}
    <div class="user-bio">
      <span>Hey <strong>{$username}</strong></span>
      <img
        src={`https://avatars.dicebear.com/api/initials/${$username}.svg`}
        alt="avatar"
      />
    </div>

    <button class="signout-button" on:click={signout}>Sign Out</button>
  {:else}
    <h3>Gun.js</h3>
  {/if}
</header>
