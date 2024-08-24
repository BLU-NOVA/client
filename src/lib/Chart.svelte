<script>
  // Data for your company
  const data = [
    { category: "Price", value: 40, color: "#ca8a04" },
    { category: "Quality", value: 100, color: "#ca8a04" },
  ];

  const maxValue = Math.max(...data.map((d) => d.value));
</script>

<div class="chart-container w-full">
  <h2 class="chart-title text-center max-md:hidden">-Our Price vs Quality-</h2>
  <div class="chart">
    {#each data as item}
      <div class="bar-container">
        <span class="bar-label">{item.category}</span>
        <div class="bar-wrapper">
          <div
            class="bar"
            style="width: {(item.value / maxValue) *
              100}%; background-color: {item.color}; height: 50px;"
          ></div>
        </div>
      </div>
    {/each}
  </div>
</div>

<style>
  .chart-container {
    width: 400px;
    margin: 20px auto;
    text-align: left;
  }

  .chart-title {
    font-size: 20px;
    margin-bottom: 20px;
    text-align: center;
  }

  .chart {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .bar-container {
    display: flex;
    align-items: center;
  }

  .bar-label {
    width: 80px;
    font-weight: bold;
    margin-right: 10px;
  }

  .bar-wrapper {
    flex-grow: 1;
    background-color: inherit;
    border-radius: 5px;
    overflow: hidden;
  }

  .bar {
    height: 30px;
    transition: width 0.5s ease-in-out;
    position: relative;
  }
</style>
