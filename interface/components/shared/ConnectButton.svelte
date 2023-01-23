<script>
  import { plugConnection } from "../connexion"
  // export let message = "Sign in"
  export let hConnectPlug
    export let principalId
    
   
</script>

<button on:click={plugConnection}>
  


  <div>
    {#if principalId}
      <p>
        Connected<span class="mobile-hide">
          &nbsp;as <span id="pid">{principalId}...</span></span
        >
      </p>
    {:else}
      Connect<span class="mobile-hide">&nbsp;plug wallet</span>
    {/if}
  </div>
</button>

