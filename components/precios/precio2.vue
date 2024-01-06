<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>Plan</th>
          <th>Description</th>
          <th>Price</th>
          <th>Action</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Basic Plan</td>
          <td>Perfect for individuals</td>
          <td class="price">$19.99/month</td>
          <td><button class="select-button">Select Plan</button></td>
        </tr>
        <tr>
          <td>Pro Plan</td>
          <td>Great for businesses</td>
          <td class="price">$49.99/month</td>
          <td><button class="select-button">Select Plan</button></td>
        </tr>
        <tr>
          <td>Premium Plan</td>
          <td>For power users</td>
          <td class="price">$99.99/month</td>
          <td><button class="select-button">Select Plan</button></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<style scoped>

table {
    width: 100%;
  border-collapse: collapse;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

th,
td {
  padding: 20px;
  text-align: center;
  border-bottom: 1px solid #e0e0e0;
}

th {
  background-color: #f4f4f4;
  border-radius: 8px 8px 0 0;
}

td {
  border-radius: 0 0 8px 8px;
}

.price {
  font-size: 24px;
  font-weight: bold;
  color: #ff6600;
}

.select-button {
  background-color: #ff6600;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease;
}

.select-button:hover {
  background-color: #e05a00;
}
</style>
