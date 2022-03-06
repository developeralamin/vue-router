<template>
    <div>
        <div v-for="job in jobs" :key="job.id" class="jobss">
         <router-link :to="{ name: 'JobDetails' ,params:{id:job.id}}" > 
              <h2>  {{ job.title }} </h2>
         </router-link>
         
        </div>
    </div>
</template>

<script>
export default {
    name: 'Vue3RouterJobs',

    data() {
        return {
            jobs:[
                {title:'FullStacK Developer',id:1,desc:'lrem'},
                {title:'MERN Developer',id:2,desc:'lrem'},
                {title:'Laravel Developer',id:3,desc:'lrem'},
                {title:'iOS Developer',id:4,desc:'lrem'},
                {title:'Android Developer',id:5,desc:'lrem'},
            ]
        };
    },


};
</script>

<style>

.jobss h2{
      background-color: antiquewhite;
    display: inline-block;
    margin: 14px;
    padding: 19px 60px 18px 48px;
}
h2 {
    margin: 0;
    padding: 0;
}

.jobss h2:hover{
   background-color: azure

}

</style>