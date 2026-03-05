<script setup>
import axios from "axios";
import { ref } from "vue";

const lists = ref([]);

const productList = async () => {
  const respone = await axios.get("https://dummyjson.com/products");
  console.log(respone.data.products);
  lists.value = respone.data.products;
};
productList();
</script>

<template>
  <!-- Our Product Section -->
  <section class="container mt-3" id="products">
    <h2 class="text-center mb-5">Our Product</h2>

    <div class="row g-4">
      <div
        class="col-md-6 col-lg-4"
        v-for="(list, index) in lists"
        :key="index"
      >
        <div class="card h-100">
          <img :src="list.thumbnail" class="card-img-top" alt="Produk 1" />
          <div class="card-body d-flex flex-column">
            <h5 class="card-title">{{ list.title }}</h5>
            <p class="card-text">
              {{ list.description }}
            </p>
            <p class="fw-bold text-primary">$ {{ list.price }}</p>
            <div class="mt-auto d-flex justify-content-between">
              <button
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#detailProdukA"
              >
              View Detail
              </button>
              <a href="#" class="btn btn-success">Buy Now</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Modal Detail Produk A -->
  <div
    class="modal fade"
    id="detailProdukA"
    tabindex="-1"
    aria-labelledby="detailProdukALabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="detailProdukALabel">Detail Produk A</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Tutup"
          ></button>
        </div>
        <div class="modal-body">
          Produk A adalah produk unggulan dengan kualitas terbaik, cocok untuk
          kebutuhan sehari-hari Anda.
        </div>
        <div class="modal-footer">
          <a href="#" class="btn btn-success">Beli Sekarang</a>
          <button
            type="button"
            class="btn btn-secondary"
            data-bs-dismiss="modal"
          >
            Tutup
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Modal Detail Produk B -->
  <div
    class="modal fade"
    id="detailProdukB"
    tabindex="-1"
    aria-labelledby="detailProdukBLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="detailProdukBLabel">Detail Produk B</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Tutup"
          ></button>
        </div>
        <div class="modal-body">
          Produk B hadir dengan desain modern dan harga terjangkau, memberikan
          nilai lebih bagi Anda.
        </div>
        <div class="modal-footer">
          <a href="#" class="btn btn-success">Beli Sekarang</a>
          <button
            type="button"
            class="btn btn-secondary"
            data-bs-dismiss="modal"
          >
            Tutup
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Modal Detail Produk C -->
  <div
    class="modal fade"
    id="detailProdukC"
    tabindex="-1"
    aria-labelledby="detailProdukCLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="detailProdukCLabel">Detail Produk C</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Tutup"
          ></button>
        </div>
        <div class="modal-body">
          Produk C menawarkan fitur premium dengan kualitas tinggi yang
          mendukung aktivitas profesional Anda.
        </div>
        <div class="modal-footer">
          <a href="#" class="btn btn-success">Beli Sekarang</a>
          <button
            type="button"
            class="btn btn-secondary"
            data-bs-dismiss="modal"
          >
            Tutup
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
