<script>
  import ApiPricingCard from "./APIPricingCard.svelte";

  const pricingPlans = [
    {
      name: "Basic",
      price: 49,
      description: "For Most Business that want to optimize their web queries",
      features: [
        "All Limited Links",
        "Own Analytics Platform",
        "Chat Support",
        "Optimized Hashtags",
        "Unlimited Users",
      ],
      isActive: false,
    },
    {
      name: "Standard",
      price: 69,
      description: "For Most Business that want to optimize their web queries",
      features: [
        "All Limited Links",
        "Own Analytics Platform",
        "Chat Support",
        "Optimized Hashtags",
        "Unlimited Users",
      ],
      isActive: true,
    },
    {
      name: "Premium",
      price: 89,
      description: "For Most Business that want to optimize their web queries",
      features: [
        "All Limited Links",
        "Own Analytics Platform",
        "Chat Support",
        "Optimized Hashtags",
        "Unlimited Users",
      ],
      isActive: false,
    },
  ];
</script>

<main style="background-color: #ebeef1" id="pricing" class="pt-4 mb-6 pb-10">
  <h1
    class="text-[#091242] text-xl flex justify-center items-center pt-6 pb-6 font-semibold"
  >
    Our Best Pricing
  </h1>

  <ApiPricingCard />

  <div class="wrapper">
    {#each pricingPlans as plan}
      <div class="card {plan.isActive ? 'active' : ''}">
        <h3>{plan.name}</h3>
        <h1>${plan.price}<span>/Month</span></h1>
        <p>{plan.description}</p>
        <ul>
          {#each plan.features as feature}
            <li>{feature}</li>
          {/each}
        </ul>
        <a href="plan">Choose Plan</a>
      </div>
    {/each}
  </div>
</main>

<style>
  .wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    color: rgba(0, 0, 0, 0.7);
  }

  .wrapper .card {
    max-width: 300px;
    background-color: white;
    padding: 40px;
    margin: 30px 15px;
    /* border-radius: 6px; */
    box-shadow:
      10px 10px 10px -1px rgba(10, 99, 169, 0.16),
      3px 3px 10px -1px rgba(255, 255, 255, 0.7);
  }

  .wrapper .card h3 {
    margin-bottom: 15px;
    color: #1c1f35;
    text-align: center;
    font: bold;
  }

  .wrapper .card.active {
    background-color: #091242;
    transform: scale(1, 1.09);
  }

  .wrapper .card.active h3 {
    color: rgba(255, 255, 255, 1);
    font: bold;
    text-align: center;
  }

  .wrapper .card h1 {
    margin-bottom: 10px;
    color: #1c1f35;
    font-size: 2.5rem;
    font: bold;
    text-align: center;
  }

  .wrapper .card.active h1 {
    color: rgba(255, 255, 255, 1);
    font: bold;
  }

  .wrapper .card h1 span {
    font-size: 12px;
    color: rgba(0, 0, 0, 0.7);
  }

  .wrapper .card.active h1 span {
    color: rgba(255, 255, 255, 0.9);
  }

  .wrapper .card p {
    margin: 20px 0;
    color: rgba(0, 0, 0, 0.6);
    font-size: 14px;
    line-height: 1.5;
  }

  .wrapper .card.active p {
    color: rgba(255, 255, 255, 1);
  }

  .wrapper .card.active li {
    color: rgba(255, 255, 255, 0.9);
  }

  .wrapper .card ul {
    list-style: none;
  }

  .wrapper .card ul li {
    line-height: 3;
    color: rgba(0, 0, 0, 0.9);
  }

  .wrapper .card a {
    margin: 20px 0;
    text-align: center;
    display: block;
    text-decoration: none;
    background-color: #091242;
    color: white;
    padding: 12px;
    transition: 0.4s;
  }

  .wrapper .card.active a {
    background: linear-gradient(to right, #ffb629, #ffd7a6);
    color: #091242;
    padding: 8px;
  }

  .wrapper .card a:hover {
    border: 1px solid #091242;
    background-color: white;
    color: #091242;
  }

  .wrapper .card.active a:hover {
    border: 1px solid white;
    background: #091242;
    color: white;
  }
</style>
