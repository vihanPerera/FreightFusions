<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import * as Select from "$lib/components/ui/select/index.js";
  import { Input } from "$lib/components/ui/input/index.js";

  const countries = [
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

  const uoms = [
    {
      value: "kg",
      label: "KG",
    },
    {
      value: "m3",
      label: "M3",
    },
    {
      value: "l",
      label: "L",
    },
    {
      value: "u",
      label: "U",
    },
  ];
</script>

<main
  id="tariff-calculator"
  class=" bg-[#091242] flex items-center justify-center py-[100px] mt-10 mb-10 z-0"
>
  <div class="bg-white shadow-lg p-8 w-full max-w-2xl">
    <h2 class="text-xl font-semibold text-center mb-2 text-[#091242]">
      Tariff Calculator
    </h2>
    <p class="text-center text-gray-600 mb-6">
      Streamline your duty calculations with our easy-to-use tool, helping you
      achieve better results
    </p>
    <form class="space-y-4">
      <div class="flex space-x-4">
        <Select.Root>
          <Select.Trigger id="origin">
            <Select.Value placeholder="Shipment Origin" />
          </Select.Trigger>
          <Select.Content>
            {#each countries as country}
              <Select.Item value={country.value} label={country.label}
                >{country.label}</Select.Item
              >
            {/each}
          </Select.Content>
        </Select.Root>
        <Select.Root>
          <Select.Trigger id="country">
            <Select.Value placeholder="Shipment Destination" />
          </Select.Trigger>
          <Select.Content>
            {#each countries as country}
              <Select.Item value={country.value} label={country.label}
                >{country.label}</Select.Item
              >
            {/each}
          </Select.Content>
        </Select.Root>
      </div>
      <Input id="name" placeholder="HS Code" />
      <div class="flex space-x-4">
        <Input id="name" placeholder="Parcel Weight" />
        <Select.Root>
          <Select.Trigger id="uom">
            <Select.Value placeholder="UOM" />
          </Select.Trigger>
          <Select.Content>
            {#each uoms as uom}
              <Select.Item value={uom.value} label={uom.label}
                >{uom.label}</Select.Item
              >
            {/each}
          </Select.Content>
        </Select.Root>
      </div>
      <div class="flex justify-center">
        <Button
          style="background: linear-gradient(to right, #FFB629, #FFD7A6);
        color: #1c1f35;
        border-radius: 0;
        padding: 8px 16px;
        border: none;
        font-size: 14px;">Calculate</Button
        >
      </div>
    </form>
  </div>
</main>
