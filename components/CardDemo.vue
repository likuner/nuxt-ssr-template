<style>
.rate-demo {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
<template>
  <h3>Card</h3>
  <Card style="width:100%">
    <template #title>
      <Icon type="ios-film-outline"></Icon>
      Classic film
    </template>
    <template #extra>
      <a href="#" @click.prevent="changeLimit">
        <Icon type="ios-loop-strong"></Icon>
        Change
      </a>
    </template>
    <p class="rate-demo" v-for="item in randomMovieList">
      <a :href="item.url" target="_blank">{{ item.name }}</a>
      <span>
                <Rate disabled v-model="item.rate" />{{ item.rate }}
            </span>
    </p>
  </Card>
</template>
<script>
export default {
  data () {
    return {
      movieList: [
        {
          name: 'The Shawshank Redemption',
          url: 'https://movie.douban.com/subject/1292052/',
          rate: 9.6
        },
        {
          name: 'Leon:The Professional',
          url: 'https://movie.douban.com/subject/1295644/',
          rate: 9.4
        },
        {
          name: 'Farewell to My Concubine',
          url: 'https://movie.douban.com/subject/1291546/',
          rate: 9.5
        },
        {
          name: 'Forrest Gump',
          url: 'https://movie.douban.com/subject/1292720/',
          rate: 9.4
        },
        {
          name: 'Life Is Beautiful',
          url: 'https://movie.douban.com/subject/1292063/',
          rate: 9.5
        },
        {
          name: 'Spirited Away',
          url: 'https://movie.douban.com/subject/1291561/',
          rate: 9.2
        },
        {
          name: 'Schindler\'s List',
          url: 'https://movie.douban.com/subject/1295124/',
          rate: 9.4
        },
        {
          name: 'The Legend of 1900',
          url: 'https://movie.douban.com/subject/1292001/',
          rate: 9.2
        },
        {
          name: 'WALL·E',
          url: 'https://movie.douban.com/subject/2131459/',
          rate: 9.3
        },
        {
          name: 'Inception',
          url: 'https://movie.douban.com/subject/3541415/',
          rate: 9.2
        }
      ],
      randomMovieList: []
    }
  },
  methods: {
    changeLimit () {
      function getArrayItems(arr, num) {
        const temp_array = [];
        for (let index in arr) {
          temp_array.push(arr[index]);
        }
        const return_array = [];
        for (let i = 0; i<num; i++) {
          if (temp_array.length>0) {
            const arrIndex = Math.floor(Math.random()*temp_array.length);
            return_array[i] = temp_array[arrIndex];
            temp_array.splice(arrIndex, 1);
          } else {
            break;
          }
        }
        return return_array;
      }
      this.randomMovieList = getArrayItems(this.movieList, 5);
    }
  },
  mounted () {
    this.changeLimit();
  }
}
</script>
