<template>
    
    <ul class="asd" >
           <li v-for="(game, index) in games">
            <p> {{ index }} <strong>{{ game.title }}</strong></p>
           </li>
    </ul>


</template>

<script>
    import axios from 'axios';
    
    export default {
        data() {
            return {
                games: []
            }
        },
        
        // Fetches games when the component is created.
        created() {
            axios.get(`json/games.json`)
                    .then(response => {
                        // JSON responses are automatically parsed.
                        this.games = response.data.gamesData
                      
                     
                    })
                    .catch(e => {
                        this.errors.push(e)
                    })
        }
    }
</script>