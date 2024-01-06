<template>
  <div>
    <div class="pricing-container">
        <div>
        <br />
        <div class="price-card">
          <h2>Premium Plan</h2>
          <p>For power users</p>
          <div class="price">$99.99/month</div>
          <button class="button">Select Plan</button>
        </div>
      </div>
      <div class="price-card">
        <h2>Pro Plan</h2>
        <p>Great for businesses</p>
        <div class="price">$49.99/month</div>
        <button class="button1">Select Plan</button>
      </div>
      <div>
        <br />
        <div class="price-card">
          <h2>Premium Plan</h2>
          <p>For power users</p>
          <div class="price">$99.99/month</div>
          <button class="button">Select Plan</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.pricing-container {
  display: flex;
  justify-content: center;
}

.price-card {
  text-align: center;
  padding: 20px;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
}

.price-card h2 {
  color: #333;
}

.price-card p {
  color: #666;
}

.price-card .price {
  font-size: 24px;
  font-weight: bold;
  margin-top: 10px;
}

.price-card .button {
  padding: 10px 20px;
  background-color: white;
  border: 1px solid blue;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease;
}
.price-card .button1 {
    color: white;
    background-color: blue;

  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease;
}
</style>
