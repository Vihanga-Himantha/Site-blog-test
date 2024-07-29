<template>
  <q-page>
    <!-- Hero Section -->
    <HeroSection
      title="Welcome to Our Website"
      subtitle="Your one-stop solution for all your needs."
      @learn-more="learnMore"
    />

    <!-- Cards Section -->
    <q-space />
    <div class="cards">
      <Card
        v-for="card in cards"
        :key="card.id"
        :title="card.title"
        :description="card.description"
        :image="card.image"
        @view-more="viewMore(card.id)"
      />
    </div>
  </q-page>
</template>

<script>
import HeroSection from 'components/HeroSection.vue';
import Card from 'components/Card.vue';

export default {
  name: 'Home',
  components: {
    HeroSection,
    Card,
  },
  data() {
    return {
      cards: [
        {
          id: 1,
          title: 'Card 1',
          description: 'This is a description for card 1.',
          image: 'src/assets/images/6.jpg',
        },
        {
          id: 2,
          title: 'Card 2',
          description: 'This is a description for card 2.',
          image: 'src/assets/images/6.jpg',
        },
        {
          id: 3,
          title: 'Card 3',
          description: 'This is a description for card 3.',
          image: 'src/assets/images/6.jpg',
        },
        {
          id: 4,
          title: 'Card 1',
          description: 'This is a description for card 1.',
          image: 'src/assets/images/6.jpg',
        },
      ],
    };
  },
  methods: {
    learnMore() {
      alert('Learn more about our services!');
    },
    viewMore(cardId) {
      alert(`View more about card ${cardId}`);
    },
  },
};
</script>

<style scoped>
.q-page {
  padding: 0 !important; /* Remove padding globally */
}

.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

@media (min-width: 600px) and (max-width: 1439.98px) {
  .q-page {
    padding: 0 !important; /* Remove padding for specific media query */
  }
}
</style>



