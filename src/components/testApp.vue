<template>
    <div>
      <h1>Coupon Information</h1>
      <div v-if="isLoading">
        <p>Loading...</p>
      </div>
      <div v-else>
        <div v-if="activeCoupons.length > 0">
          <h2>Active Coupons:</h2>
          <ul>
            <li v-for="(coupon, index) in activeCoupons" :key="index">
              <p>{{ coupon.name }}</p>
              <p>Start Date: {{ coupon.start_date }}</p>
              <p>End Date: {{ coupon.end_date }}</p>
            </li>
          </ul>
        </div>
        <div v-else>
          <p>No active coupons available.</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isLoading: true,
        activeCoupons: []
      };
    },
    mounted() {
      // クーポン情報を取得
      this.fetchActiveCoupons();
    },
    methods: {
      async fetchActiveCoupons() {
        try {
          const response = await fetch('/store_active_coupons');
          const data = await response.json();
          // クーポン情報を取得できたかどうかを判定
          if (Array.isArray(data) && data.length > 0) {
            this.activeCoupons = data;
          } else {
            // クーポン情報が取得できなかった場合の処理
            console.log('No active coupons available.');
          }
        } catch (error) {
          console.error('Error fetching active coupons:', error);
        } finally {
          this.isLoading = false;
        }
      }
    }
  };
  </script>
  