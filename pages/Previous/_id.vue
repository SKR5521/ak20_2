<template>
    <div>
        <h1>This is anprevious year with id {{ $route.params.id}}</h1>

        <stats :pageid="$route.params.id" />
    </div>
    
</template>

<script>
import stats from '@/components/jsf/stats'

export default {
    components:{
        stats
    }
  

}
</script>