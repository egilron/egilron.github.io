# Demo AI-søk i foross
Teste funksjonaliteten. Søket gjøres i en tekstbase der all formatering er borte.

<!-- Widget JavaScript bundle -->
<script src="https://cloud.google.com/ai/gen-app-builder/client?hl=en_US"></script>

<!-- Search widget element is not visible by default -->
<gen-search-widget
  configId="27042130-fba4-470d-9718-cb3a5660dd04"
  triggerId="searchWidgetTrigger">
</gen-search-widget>

<!-- Element that opens the widget on click. It does not have to be an input -->
<input placeholder="Search here" id="searchWidgetTrigger" />
