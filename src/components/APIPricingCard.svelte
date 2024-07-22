<script>
</script>

<main>
  <div style="display: flex; justify-content: center; margin-bottom: 2rem">
    <div class="apicard">
      <div class="apicard-header tariff-search">Tariff Code Search API</div>
      <div class="apicard-body">
        <div class="price">
          $0.10
          <span>Per API Call</span>
        </div>
      </div>
    </div>
    <div class="apicard">
      <div class="apicard-header tariff-calc">Tariff Calculation API</div>
      <div class="apicard-body">
        <div class="price">
          $0.12
          <span>Per API Call</span>
        </div>
      </div>
    </div>
  </div>
</main>

<style>
  .apicard {
    overflow: hidden;
    width: 600px;
    margin: 10px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  .apicard-header {
    padding: 10px;
    color: white;
    text-align: center;
    font-size: 18px;
  }
  .apicard-body {
    padding: 18px;
    text-align: center;
  }
  .tariff-search {
    background-color: #ffb629;
  }
  .tariff-calc {
    background-color: #091242;
  }
  .price {
    font-size: 40px;
    /* font-weight: bold; */
    color: #1c1f35;
  }
  .price span {
    display: block;
    font-size: 16px;
    color: #1c1f35;
    margin-top: 5px;
  }
</style>
