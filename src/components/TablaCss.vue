<template> 
    <table>
        <thead>
            <tr>
                <th scope="col" class="inicio">#</th>
                <th scope="col">01</th>
                <th scope="col">02</th>
                <th scope="col">03</th>
                <th scope="col">04</th>
                <th scope="col">05</th>
                <th scope="col">06</th>
                <th scope="col">07</th>
                <th scope="col">08</th>
                <th scope="col">09</th>
                <th scope="col">10</th>
                <th scope="col">11</th>
                <th scope="col">12</th>
                <th scope="col">13</th>
                <th scope="col">14</th>
                <th scope="col">15</th>
                <th scope="col">16</th>
                <th scope="col">17</th>
                <th scope="col">18</th>
                <th scope="col">19</th>
                <th scope="col">20</th>
                <th scope="col">21</th>
                <th scope="col">22</th>
                <th scope="col">23</th>
                <th scope="col">24</th>
                <th scope="col">25</th>
            </tr>
        </thead>
        <tbody>
            <tr class="home">
                <td class="inicio">C</td>
                <td>01</td>
                <td>02</td>
                <td>x</td>
                <td>x</td>
                <td>03</td>
                <td>04</td>
                <td>x</td>
                <td>x</td>
                <td>05</td>
                <td>06</td>
                <td>07</td>
                <td>08</td>
                <td>x</td>
                <td>x</td>
                <td>x</td>
                <td>09</td>
                <td>10</td>
                <td>11</td>
                <td>12</td>
                <td>13</td>
                <td>x</td>
                <td>x</td>
                <td>14</td>
                <td>15</td>
                <td>16</td>
            </tr>
            <tr class="guest">
                <td class="inicio">V</td>
                <td>x</td>
                <td>x</td>
                <td>01</td>
                <td>02</td>
                <td>x</td>
                <td>x</td>
                <td>03</td>
                <td>04</td>
                <td>x</td>
                <td>x</td>
                <td>x</td>
                <td>x</td>
                <td>05</td>
                <td>06</td>
                <td>07</td>
                <td>x</td>
                <td>x</td>
                <td>x</td>
                <td>x</td>
                <td>x</td>
                <td>08</td>
                <td>09</td>
                <td>x</td>
                <td>x</td>
                <td>x</td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>

</script>

<style scoped>
table {
    font-size: small;
    table-layout: fixed;
    border-collapse: collapse;
    
}
table thead tr{
    background-color: #303030;
    color: white;
    
}
table tr{
    border: 2px #909090 solid;
}
table td,th{
    padding: 5px;
    text-align: center;
    font-weight: normal;
    border: 1px #909090 dotted;
}
.home {
    color: blue;
}
.guest{
    color: red;
}
.inicio{
    font-weight: bold;
    background-color: grey;
    padding-right: 10px;
}
</style>