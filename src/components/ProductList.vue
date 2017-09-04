<template>
  <div>
    <h1>{{ title }}</h1>
    
    <div>
        <table class="product-table">
            <colgroup>
                <col>
                <col>
                <col>
                <col>
            </colgroup>
            <tbody>
                <tr>
                    <th scope="row">
                        <p>이용기간</p>
                        <select v-model="selected">
                            <option v-for="option in options" v-bind:value="option.value">
                                {{ option.text }}
                            </option>     
                        </select>
                    </th>
                    <!-- loop 돌릴 부분 -->
                    <td v-for="productlist in productlists">
                        <p class="product-type"> {{ productlist.producttype }}</p>
                        <p class="discount" v-if="selected >= 12">
                            <span>16.6%할인</span>
                            <span><s>{{ (productlist.price*selected).toLocaleString('ko') }}원</s></span>
                        </p>
                        <p class="price" v-if="selected >= 12">
                            {{ (Math.ceil((productlist.price*selected)  - (productlist.price*selected*0.1666666666667))).toLocaleString('ko')}}원
                        </p>
                        <p class="price" v-else>
                            {{ (productlist.price*selected).toLocaleString('ko') }}원
                        </p>
                        <button role="button">신청하기</button>
                    </td>
                </tr>
                <tr>
                    <th scope="row">트래픽</th>
                    <td>
                        <p>180GB(월)</p>
                        <p>6GB(일)</p>
                    </td>
                    <td>무제한</td>
                    <td>무제한</td>
                </tr>
                <tr>
                    <th scope="row">웹</th>
                    <td>5GB</td>
                    <td>5GB</td>
                    <td>20GB</td>
                </tr>
                <tr>
                    <th scope="row">DB</th>
                    <td>
                        <p>무제한</p>
                        <p>동시 허용 접속수 30conn.</p>
                    </td>
                    <td>
                        <p>무제한</p>
                        <p>동시 허용 접속수 30conn.</p>
                    </td>
                    <td>
                        <p>무제한</p>
                        <p>동시 허용 접속수 30conn.</p>
                    </td>
                </tr>
                <tr>
                    <th scope="row">메일</th>
                    <td>5개/5GB</td>
                    <td>5개/5GB</td>
                    <td>5개/5GB</td>
                </tr>
                <tr>
                    <th scope="row">설치비</th>
                    <td>
                        <p>10,000원</p>
                        <p>(타사 도메인 30,000원)</p>
                    </td>
                    <td>
                        <p>10,000원</p>
                        <p>(타사 도메인 30,000원)</p>
                    </td>
                    <td>
                        <p>10,000원</p>
                        <p>(타사 도메인 30,000원)</p>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'product-list',
  
  data: function () {
   return { 
    title: '기업형',
    selected: 12,
    options: [
        {text: '1개월', value: 1},
        {text: '3개월', value: 3},
        {text: '12개월', value: 12},
        {text: '24개월', value: 24}
    ],
    productlists: 
    [
      {producttype: '스탠더드', price: 15000},
      {producttype: '스탠더드 무제한', price: 20000},
      {producttype: '프리미엄 무제한', price: 50000}
    ]
   }
  }
}

</script>
<style lang="scss">
$table-head-bg: #ccc;

h1 {
    font-weight: normal;
    font-size: 18px;
}
.product-table {
    table-layout: fixed;

    width: 100%;
    tr {
        &:first-child > th,
        &:first-child > td {
            background: $table-head-bg;
        }
    }
    th {
        
    }
}
</style>

