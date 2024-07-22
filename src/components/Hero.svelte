<!-- <script>
  let heading = "Capture Photography";
  let message = "I capture moments in nature and keep them alive";
</script>

<main>
  <div
    class="flex items-center justify-center h-screen mb-[10rem] bg-fixed bg-center bg-cover custom-img"
  >
    <div class="absolute top-0 left-0 right-0 bottom-0 bg-black/55 z-[2]" />
    <div class="p-5 text-white z-[2] mt-[-10rem]">
      <h2 class="text-5xl font-bold">{heading}</h2>
      <p class="py-5 text-xl">{message}</p>
      <button class="px-8 py-2 border">Book</button>
    </div>
  </div>
</main> -->

<script lang="ts">
  let heading = "Connecting You to Every Corner of the World";
  let message =
    "Seamless connectivity at your fingertips. Stay connected and explore endless possibilities";
  import { Button } from "$lib/components/ui/button/index.js";
  import * as Select from "$lib/components/ui/select/index.js";
  import { Input } from "$lib/components/ui/input/index.js";
  import * as RadioGroup from "$lib/components/ui/radio-group/index.js";
  import { Label } from "$lib/components/ui/label/index.js";

  const countries1 = [
    {
      value: "australia",
      label: "Australia",
    },
    {
      value: "china",
      label: "China",
    },
    {
      value: "japan",
      label: "Japan",
    },
    {
      value: "sriLanka",
      label: "Sri Lanka",
    },
  ];
</script>

<main id="home">
  <div class="video-container">
    <video autoplay muted loop id="background-video">
      <source src="/video1.mp4" type="video/mp4" />
      Your browser does not support the video tag.
    </video>
    <div class="overlay">
      <div class="content">
        <h2 class="text-5xl font-bold">{heading}</h2>
        <p class="py-5 text-xl">{message}</p>
        <div class="bg-white shadow-lg p-8 w-full max-w-[1800px] mt-8 px-10">
          <form class="space-y-4">
            <div class="flex items-center space-x-4">
              <RadioGroup.Root value="option-one">
                <div class="flex items-center space-x-4">
                  <RadioGroup.Item value="option-one" id="option-one" />
                  <Label for="option-one" style="color: #757575">Import</Label>
                  <RadioGroup.Item value="option-two" id="option-two" />
                  <Label for="option-two" style="color: #757575">Export</Label>
                </div>
              </RadioGroup.Root>
            </div>
            <div class="flex space-x-4">
              <Select.Root>
                <Select.Trigger id="origin1">
                  <Select.Value placeholder="Shipment Origin" />
                </Select.Trigger>
                <Select.Content>
                  {#each countries1 as country}
                    <Select.Item value={country.value} label={country.label}
                      >{country.label}</Select.Item
                    >
                  {/each}
                </Select.Content>
              </Select.Root>
              <Select.Root>
                <Select.Trigger id="destination1">
                  <Select.Value placeholder="Shipment Destination" />
                </Select.Trigger>
                <Select.Content>
                  {#each countries1 as country}
                    <Select.Item value={country.value} label={country.label}
                      >{country.label}</Select.Item
                    >
                  {/each}
                </Select.Content>
              </Select.Root>
              <Input id="name" placeholder="Enter Product Name or HS Code" />
              <Button
                style="background: linear-gradient(to right, #FFB629, #FFD7A6);
            color: #1c1f35;
            border-radius: 0;
            padding: 8px 16px;
            border: none;
            font-size: 14px;">Search</Button
              >
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</main>

<style>
  .video-container {
    position: relative;
    height: 100vh;
    overflow: hidden;
  }

  #background-video {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transform: translate(-50%, -50%);
    z-index: 1;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.55);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2;
  }

  .content {
    text-align: center;
    color: white;
  }
</style>
