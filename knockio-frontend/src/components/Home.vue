<template>
    <div>
        <h1 class="jumbotron">Home</h1>
        <div class="split left">
            <section id="stream">
                <h4>Stream</h4>
                <img src="@/assets/logo.jpg" width="800" length="600" id="stream">
                <div id="streamOptions">
                    <ul>                
                        <li><button @click="addItem">Grab Still</button></li>
                        <li><button>Buzz</button></li>
                    </ul>
                </div>
            </section>
        </div>
        <div class="split right">
            <h4>Saved Screenshots</h4>
            <table>
            <tr>
                <th>Date Saved</th>
                <th>Image File</th>
            </tr>
            <tr v-for="(tableData,k) in tableData" :key="k">
                <td>{{tableData.datetime}}</td>
                <td><a href="#">{{tableData.image}}</a></td>
            </tr>
            </table>
        </div>
    </div>
</template>

<script>
var count=0;
export default {
    name: 'Home',
    data:{
        datetime: '',
        image: '',
    },
    data(){
        return {
          tableData: [],
        }
    },
    methods:{
        addItem(){
            var today = new Date();
            var screenshot = document.images[0].src;
            if(count<30){
                this.tableData.push({
                    datetime: today.toLocaleString(),
                    image: "screenshot " + (count+1),
                });
            }
            count++
        }
    }
}
</script>