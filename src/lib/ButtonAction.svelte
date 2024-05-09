<script>

  export let text = 'click me';

  async function getDataPlease(){
    let a = await fetch('https://expressapp-two.vercel.app')
      .then((res)=>{
        return JSON.parse(res);
      }).then((data)=>{
        console.log(data);
      }).catch((err)=>{
        console.error(err);
      })
  }
</script>


<button on:click={getDataPlease}>
  { text }
</button>


<style lang="scss">
  button {
    border-radius: 8px;
    border: 1px solid transparent;
    padding: 0.6em 1.2em;
    font-size: 1em;
    font-weight: 500;
    font-family: inherit;
    background-color: #1a1a1a;
    cursor: pointer;
    transition: border-color 0.25s;
  }
  button:hover {
    border-color: #646cff;
  }
  button:focus,
  button:focus-visible {
    outline: 4px auto -webkit-focus-ring-color;
  }

  .navBtn {
    background-color: #f0f0f0;
    color: #1a1a1a;
  }

  @media (prefers-color-scheme: light) {
    button {
      background-color: #f9f9f9;
    }
}


</style>