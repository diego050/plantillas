<template>
  <div class="container">
    <br />
    <div class="pricing-container">
      <div class="col-8">
        <h2>Lorem ipsum dolor sit amet</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua.
        </p>
        <h3> Lorem ipsum</h3>
        <div class="columns">
            <div style="margin-bottom: 20px;">lorem ipsum</div>
            <div style="margin-bottom: 20px;">lorem ipsum</div>
            <div>lorem ipsum</div>
            <div>lorem ipsum</div>
        </div>
      </div>
      <div class="col-4">
        <div class="price-card">
          <p>Lorem ipsum dolor</p>
          <p style="font-size: 50px; margin: 0">$325</p>
          <br />
          <button>Select Plan</button>
          <br />
          <div class="price" align="justify">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua</div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.columns {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  column-gap: 10px;
}
.pricing-container {
  display: flex;
  background-color: #fff;
  padding: 20px;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  border-radius: 8px;
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
  font-size: 16px;
  color: black;
  margin-top: 10px;
}

.price-card button {
  background-color: blue;
  color: #fff;
  padding: 10px 70px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease;
}

.price-card button:hover {
  background-color: #e05a00;
}
</style>
