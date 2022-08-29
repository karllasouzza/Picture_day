<script setup>
defineProps({ transcribe: Boolean });
</script>

<template>
  <svg
    width="30"
    height="30"
    v-if="!transcribe"
    viewBox="0 0 24 24"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M15.7161 16.2234H8.49609"
      stroke="#eee"
      stroke-width="1.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M15.7161 12.0369H8.49609"
      stroke="#eee"
      stroke-width="1.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M11.2511 7.86011H8.49609"
      stroke="#eee"
      stroke-width="1.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M15.9085 2.74982C15.9085 2.74982 8.23149 2.75382 8.21949 2.75382C5.45949 2.77082 3.75049 4.58682 3.75049 7.35682V16.5528C3.75049 19.3368 5.47249 21.1598 8.25649 21.1598C8.25649 21.1598 15.9325 21.1568 15.9455 21.1568C18.7055 21.1398 20.4155 19.3228 20.4155 16.5528V7.35682C20.4155 4.57282 18.6925 2.74982 15.9085 2.74982Z"
      stroke="#eee"
      stroke-width="1.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>

  <svg
    width="30"
    height="30"
    viewBox="0 0 24 24"
    fill="none"
    v-else
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M16.3028 2.74982H7.65076C4.63876 2.74982 2.74976 4.88382 2.74976 7.90382V16.0498C2.74976 19.0698 4.63076 21.2038 7.65076 21.2038H16.2978C19.3228 21.2038 21.2028 19.0698 21.2028 16.0498V7.90382C21.2068 4.88382 19.3258 2.74982 16.3028 2.74982Z"
      stroke="#eee"
      stroke-width="1.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M10.7031 8.78503C10.7031 9.80503 9.87711 10.631 8.85711 10.631C7.83811 10.631 7.01111 9.80503 7.01111 8.78503C7.01111 7.76503 7.83811 6.93903 8.85711 6.93903C9.87611 6.94003 10.7021 7.76603 10.7031 8.78503Z"
      stroke="#eee"
      stroke-width="1.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M21.207 14.951C20.284 14.001 18.509 12.082 16.579 12.082C14.648 12.082 13.535 16.315 11.678 16.315C9.821 16.315 8.134 14.401 6.646 15.628C5.158 16.854 3.75 19.361 3.75 19.361"
      stroke="#eee"
      stroke-width="1.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>

<style></style>
