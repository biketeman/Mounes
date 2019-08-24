<template>
  <div>
    <h1>hey!</h1>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      numberOfRound: 0
    }
  },
  methods: {

    giveCards () {
      const cards = ['7 coeur', '8 coeur', '9 coeur', '10 coeur', 'V coeur', 'D coeur', 'R coeur', 'A coeur',
        '7 pic', '8 pic', '9 pic', '10 pic', 'V pic', 'D pic', 'R pic', 'A pic',
        '7 carreau', '8 carreau', '9 carreau', '10 carreau', 'V carreau', 'D carreau', 'R carreau', 'A carreau',
        '7 trèfle', '8 trèfle', '9 trèfle', '10 trèfle', 'V trèfle', 'D trèfle', 'R trèfle', 'A trèfle']
      console.log(cards)
      randomCards()

      function randomCards () {
        let randomNumber = Math.round(Math.random() * cards.length)
        let randomCard = cards[randomNumber]
        console.log(randomNumber)
        console.log(randomCard)
        cards.splice(cards.indexOf(randomCard), 1)
        console.log(cards)
      }
    }
  },
  mounted () {
    this.giveCards()
  }
}
</script>
<style lang="scss" scoped>

</style>
