<template>
    <div>
        <h2>Simple Calendar</h2>

<table>
    <thead>
        <tr>
            <th>Sun</th>
            <th>Mon</th>
            <th>Tue</th>
            <th>Wed</th>
            <th>Thu</th>
            <th>Fri</th>
            <th>Sat</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td>1</td>
            <td>2</td>
        </tr>
        <tr>
            <td>3</td>
            <td>4</td>
            <td>5</td>
            <td>6</td>
            <td>7</td>
            <td>8</td>
            <td>9</td>
        </tr>
        <!-- Add more rows for the rest of the calendar -->
    </tbody>
</table>
    </div>
</template>
<style scoped>
body {
    font-family: 'Arial', sans-serif;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
}

th, td {
    border: 1px solid #dddddd;
    text-align: center;
    padding: 8px;
}

th {
    background-color: #f2f2f2;
}

td {
    height: 100px;
}
</style>