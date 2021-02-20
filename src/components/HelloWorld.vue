<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <section class="product-list">
      <h1>Product</h1>

      <div class="product-container">
        <!-- First product  -->
        <div class="card">
          <div class="title">Lays Picanna</div>
          <div class="image">
            <img
              src="https://st2.depositphotos.com/3053449/12431/i/950/depositphotos_124319942-stock-photo-frito-lay-chips.jpg"
              alt=""
            />
          </div>
          <div class="text">50 ฿</div>
          <div>
            <div class="minus-plus">
              <i
                class="fa fa-minus-square"
                v-on:click="items.product1 -= 1"
              ></i>
              <p v-if="items.product1 >= 0">{{ items.product1 }}</p>
              <p v-else>0</p>
              <i class="fa fa-plus-square" v-on:click="items.product1 += 1"></i>
            </div>
            <button class="buy-button" @click="isShowing ^= true">
              Add Now
            </button>
          </div>
        </div>
        <!-- Second product  -->
        <div class="card">
          <div class="title">Lays Wavy</div>
          <div class="image">
            <img
              src="https://st2.depositphotos.com/3053449/12431/i/950/depositphotos_124319944-stock-photo-frito-lay-chips.jpg"
              alt=""
            />
          </div>
          <div class="text">50 ฿</div>
          <div>
            <div class="minus-plus">
              <i
                class="fa fa-minus-square"
                v-on:click="items.product2 -= 1"
              ></i>
              <p v-if="items.product2 >= 0">{{ items.product2 }}</p>
              <p v-else>0</p>
              <i class="fa fa-plus-square" v-on:click="items.product2 += 1"></i>
            </div>
            <button class="buy-button" @click="isShowing1 ^= true">
              Add Now
            </button>
          </div>
        </div>
        <!-- Third product  -->
        <div class="card">
          <div class="title">Lays Sour & Onion</div>
          <div class="image">
            <img
              src="https://st2.depositphotos.com/3053449/6553/i/950/depositphotos_65533325-stock-photo-lays-chips.jpg"
              alt=""
            />
          </div>
          <div class="text">50 ฿</div>
          <div>
            <div class="minus-plus">
              <i
                class="fa fa-minus-square"
                v-on:click="items.product3 -= 1"
              ></i>
              <p v-if="items.product3 >= 0">{{ items.product3 }}</p>
              <p v-else>0</p>
              <i class="fa fa-plus-square" v-on:click="items.product3 += 1"></i>
            </div>
            <button class="buy-button" @click="isShowing2 ^= true">
              Add Now
            </button>
          </div>
        </div>
        <!-- Fourth product -->
        <div class="card">
          <div class="title">Ruffles</div>
          <div class="image">
            <img
              src="https://st3.depositphotos.com/3053449/33347/i/1600/depositphotos_333473232-stock-photo-package-of-food.jpg"
              alt=""
            />
          </div>
          <div class="text">40 ฿</div>
          <div>
            <div class="minus-plus">
              <i
                class="fa fa-minus-square"
                v-on:click="items.product4 -= 1"
              ></i>
              <p v-if="items.product4 >= 0">{{ items.product4 }}</p>
              <p v-else>0</p>
              <i class="fa fa-plus-square" v-on:click="items.product4 += 1"></i>
            </div>
            <button class="buy-button" @click="isShowing3 ^= true">
              Add Now
            </button>
          </div>
        </div>
        <!-- Five product -->
        <div class="card">
          <div class="title">Snausages</div>
          <div class="image">
            <img
              src="https://st3.depositphotos.com/3053449/16511/i/1600/depositphotos_165118588-stock-photo-dog-treats-isolated.jpg"
              alt=""
            />
          </div>
          <div class="text">40 ฿</div>
          <div>
            <div class="minus-plus">
              <i
                class="fa fa-minus-square"
                v-on:click="items.product5 -= 1"
              ></i>
              <p v-if="items.product5 >= 0">{{ items.product5 }}</p>
              <p v-else>0</p>
              <i class="fa fa-plus-square" v-on:click="items.product5 += 1"></i>
            </div>
            <button class="buy-button" @click="isShowing4 ^= true">
              Add Now
            </button>
          </div>
        </div>
        <!-- Six product -->
        <div class="card">
          <div class="title">Sage&Valley</div>
          <div class="image">
            <img
              src="https://st3.depositphotos.com/3053449/18113/i/1600/depositphotos_181139362-stock-photo-bag-of-chips.jpg"
              alt=""
            />
          </div>
          <div class="text">40 ฿</div>
          <div>
            <div class="minus-plus">
              <i
                class="fa fa-minus-square"
                v-on:click="items.product6 -= 1"
              ></i>
              <p v-if="items.product6 >= 0">{{ items.product6 }}</p>
              <p v-else>0</p>
              <i class="fa fa-plus-square" v-on:click="items.product6 += 1"></i>
            </div>
            <button class="buy-button" @click="isShowing5 ^= true">
              Add Now
            </button>
          </div>
        </div>
      </div>

      <div class="card-product">
        <div class="small-container">
          <table>
            <tr>
              <th>Product</th>
              <th>Quantty</th>
              <th>Subtotal</th>
            </tr>
            <tr>
              <td v-show="isShowing">Lays Picanna</td>
              <td v-if="items.product2 >= 0" v-show="isShowing">
                {{ items.product1 }}
              </td>
              <td v-if="items.product1 * items.price1 >= 0" v-show="isShowing">
                {{ items.product1 * items.price1 }}
              </td>
            </tr>
            <tr>
              <td v-show="isShowing1">Lay Wavy</td>
              <td v-if="items.product2 >= 0" v-show="isShowing1">
                {{ items.product2 }}
              </td>
              <td v-if="items.product2 * items.price2 >= 0" v-show="isShowing1">
                {{ items.product2 * items.price2 }}
              </td>
            </tr>
            <tr>
              <td v-show="isShowing2">Lay Sour & Onion</td>
              <td v-if="items.product3 >= 0" v-show="isShowing2">
                {{ items.product3 }}
              </td>
              <td v-if="items.product3 * items.price3 >= 0" v-show="isShowing2">
                {{ items.product3 * items.price3 }}
              </td>
            </tr>
            <tr>
              <td v-show="isShowing3">Ruffles</td>
              <td v-if="items.product4 >= 0" v-show="isShowing3">
                {{ items.product4 }}
              </td>
              <td v-if="items.product4 * items.price4 >= 0" v-show="isShowing3">
                {{ items.product4 * items.price4 }}
              </td>
            </tr>
            <tr>
              <td v-show="isShowing4">Snausages</td>
              <td v-if="items.product5 >= 0" v-show="isShowing4">
                {{ items.product5 }}
              </td>
              <td v-if="items.product5 * items.price5 >= 0" v-show="isShowing4">
                {{ items.product5 * items.price5 }}
              </td>
            </tr>
            <tr>
              <td v-show="isShowing5">Sage&Valley</td>
              <td v-if="items.product6 >= 0" v-show="isShowing5">
                {{ items.product6 }}
              </td>
              <td v-if="items.product6 * items.price6 >= 0" v-show="isShowing5">
                {{ items.product6 * items.price6 }}
              </td>
            </tr>
            <td></td>
            <td>Total</td>
            <td
              v-if="
                items.product1 * items.price1 +
                  items.product2 * items.price2 +
                  items.product3 * items.price3 +
                  items.product4 * items.price4 +
                  items.product5 * items.price5 +
                  items.product6 * items.price6 >=
                0
              "
            >
              {{
                items.product1 * items.price1 +
                items.product2 * items.price2 +
                items.product3 * items.price3 +
                items.product4 * items.price4 +
                items.product5 * items.price5 +
                items.product6 * items.price6
              }}
            </td>
            <td v-else>0</td>
          </table>
        </div>

        <button
          class="buy-buttons"
          v-on:click="say('Order successfully Thank For Buy')"
        >
          Accept
        </button>
        <button class="buy-buttons" onClick="javascipt:location.reload()">
          Cancel
        </button>
      </div>
    </section>
    <div class="footer">
      <p>Waiting Update</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      items: {
        product1: 0,
        price1: 50,
        product2: 0,
        price2: 50,
        product3: 0,
        price3: 50,
        product4: 0,
        price4: 40,
        product5: 0,
        price5: 40,
        product6: 0,
        price6: 40,
      },
      isShowing: false,
      isShowing1: false,
      isShowing2: false,
      isShowing3: false,
      isShowing4: false,
      isShowing5: false,
    };
  },

  methods: {
    say: function (message) {
      alert(message);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer {
  width: 100%;
  height: 50px;
  background-color: #5d4954;
  color: white;
  text-align: center;
  margin-top: 2rem;
  scrollbar-shadow-color: 0px 10 px 5px black;
  padding: 5em;
}
.footer p {
  font-family: cursive;
  text-shadow: 0px 5px 5px black;
}
.product-list {
  background: #dfe6e9;
  max-width: 100%;
  text-align: center;
}
.product-list h1 {
  font-size: 30px;
  font-family: cursive;
  height: 10rem;
  font-weight: bold;
  margin-top: 10rem;
}
.product-list .card {
  background-color: white;
  border-radius: 10px;
  padding: 1em;
  box-shadow: 0px 10px 5px #b2bec3;
  text-align: center;
  font-family: cursive;
}
.card .title {
  font-size: 25px;
  font-weight: bold;
}
.card img {
  max-width: 100%;
  border-radius: 5px;
  height: 15rem;
}
.card .text {
  text-align: center;
  margin-left: 2em;
  margin-bottom: 1em;
  font-size: 13px;
}
.buy-button {
  background-color: #f9ca24;
  border: none;
  padding: 1em;
  border-radius: 5px;
  font-weight: bold;
  width: 50%;
}
.buy-buttons {
  background-color: #f9ca24;
  border: none;
  padding: 5px;
  border-radius: 20px;
  font-weight: bold;
  font-size: 10px;
  width: 15%;
  font-family: cursive;
  margin-left: 50px;
}
.buy-buttons:hover {
  box-shadow: 0px 5px 5px #b2bec3;
  color: #eb4d4b;
}
.buy-button:hover {
  box-shadow: 0px 5px 5px #b2bec3;
  color: #eb4d4b;
}
.product-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 20px;
  grid-row-gap: 40px;
  max-width: 80%;
  margin-left: 9rem;
}
.card-product {
  background-color: white;
  border-radius: 10px;
  padding: 1em;
  box-shadow: 0px 10px 5px #b2bec3;
  font-family: cursive;
  width: 60%;
  margin-top: 3rem;
  margin-left: 9rem;
}
.small-container {
  margin: 10px auto;
}
table {
  width: 100%;
  border-collapse: collapse;
}
tr {
  color: rgb(25, 10, 10);
  justify-content: space-around;
  text-align: center;
  font-size: 15px;
  font-weight: bold;
}
th {
  font-size: 18px;
}
td {
  color: #5d4954;
  font-size: 13px;
}
.minus-plus {
  display: flex;
  align-items: center;
  margin-left: 0rem;
  margin-bottom: 1em;
  justify-content: space-around;
}
.minus-plus .fa-minus-square {
  color: black;
}
.minus-plus .fa-plus-square {
  color: black;
}
@media only screen and (max-width: 1050px) {
  .product-list {
    margin-right: 5em;
  }
}
@media only screen and (max-width: 770px) {
  .product-container {
    margin-left: 0.4rem;
    grid-template-columns: 1fr 1fr;
    max-width: 97%;
  }
  .card .title {
    font-size: 15px;
  }
  .card img {
    height: 15rem;
  }
  .buy-button {
    width: 70%;
  }
  .product-list {
    margin-right: 0em;
  }
}
@media only screen and (max-width: 500px) {
  .product-container {
    margin-left: 0.4rem;
    grid-template-columns: 1fr 1fr;
    max-width: 97%;
  }
  .card .title {
    font-size: 15px;
  }
  .card img {
    height: 15rem;
  }
  .buy-button {
    width: 70%;
  }
  .card-product {
    width: 90%;
    margin-left: 1.5rem;
  }
  .product-list {
    margin-right: 0em;
  }
}
</style>