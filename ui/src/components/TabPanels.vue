<template>
  <div class="tabs-panel-container mt-3 p-8">
    <div class="container mx-auto">
      <div v-if="panel === 'getting-started'">
        <GettingStartedPanel :data="data" />
      </div>
      <div v-if="panel === 'tools'">
        <ToolsPanel :data="data" />
      </div>
      <div v-if="panel === 'extensions'">
        <ExtensionsPanel :data="data" />
      </div>
    </div>
  </div>
</template>

<script>
import GettingStartedPanel from "./panels/GettingStartedPanel";
import ToolsPanel from "./panels/ToolsPanel";
import ExtensionsPanel from "./panels/ExtensionsPanel";

export default {
  name: "TabPanels",
  components: {
    ExtensionsPanel,
    GettingStartedPanel,
    ToolsPanel,
  },
  props: {
    panel: String,
    data: Object,
  },
};
</script>
