<script>
    import { dao } from "../../src/declarations/dao"
import { plugConnection } from "./connexion";

let props = []

async function showmeprops() {

let props = dao.get_all_proposals()
console.log(props)
return props

}

async function get_all_proposals() {
    let dao = get(daoActor);
    if (!dao) {
      return
    }
    console.log("Principal", principal)
    let res = await dao.get_all_proposals()
    console.log("Proposals", res)
    return res
  }
  let promise =  get_all_proposals()


</script>

<main>

    <!-- <div class="container">        
        {#each props as prop}
    
        <div class="proposals">
            <a href={prop[1]} target="_blank" alt=ok>
            <p>{min[1]}</p><img src={min[1]} alt= hero> 
            </a>    
            </div> 
            {/each}
        </div> -->

<div class=props>
<button on:click= {showmeprops}>Show Me Proposals</button>

</div>


</main>

<style>

.props {
  display: flex;
  justify-content: center;
  gap: 0.5em;
  flex-flow: row wrap;
  max-width: 40vw;
  margin: auto;
  align-items: baseline;
  border: solid 1 px white
  
}

</style>