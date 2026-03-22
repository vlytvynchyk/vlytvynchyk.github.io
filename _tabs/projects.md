---
layout: page
icon: fas fa-toolbox
order: 0
---

## Lab

<div class="card-wrapper">
  <div class="card-item">
    <h3><a href="https://github.com/vlytvynchyk/rag-vs-long-context" target="_blank">RAG vs Long Context</a></h3>
    <p>Benchmark comparing RAG, Long Context, and No Context approaches for LLM-based documentation Q&A. Tested on FastAPI docs (~117K tokens) with local models via Ollama.</p>
  </div>
</div>

## Tools

<div class="card-wrapper">
  <div class="card-item">
    <h3><a href="https://vlytvynchyk.github.io/led-grid-builder/" target="_blank">LED Grid Builder</a></h3>
    <p>Visual web app to design and preview LED grids for MAX7219 modules. Supports multiple grid sizes, colors, icons, scrolling, and blinking effects.</p>
  </div>

  <div class="card-item">
    <h3><a href="https://vlytvynchyk.github.io/fudokan-timer-interval/" target="_blank">Fudokan Timer</a></h3>
    <p>Interval timer for karate training. Preset and custom profiles, color-coded phases, audio alerts, and vibration feedback. Supports English, Ukrainian, and Japanese.</p>
  </div>

  <div class="card-item">
    <h3><a href="https://vlytvynchyk.github.io/agent-protocols-graph/" target="_blank">Agent Protocols Graph</a></h3>
    <p>Interactive knowledge graph covering MCP, A2A, Skills, and other AI agent protocols. 23 topics, 19 courses with quizzes, spaced repetition, and a daily crawler that keeps content up to date.</p>
  </div>

  <div class="card-item">
    <h3><a href="https://github.com/vlytvynchyk/ultimate-perf-switch" target="_blank">UltimatePerfSwitch</a></h3>
    <p>System tray app that toggles the hidden Ultimate Performance power plan on Windows 11. Auto-switches based on CPU load and auto-restores the plan when Windows removes it.</p>
  </div>
</div>

## Packages

<div class="card-wrapper">
  <div class="card-item">
    <h3><a href="https://www.nuget.org/packages/DiskScout" target="_blank">DiskScout</a></h3>
    <p>Fast disk usage analyzer CLI tool. Parallel scanning, color-coded charts, space waster detection, and cleanup suggestions. Available as a standalone binary or .NET tool.</p>
    <p><code>dotnet tool install -g DiskScout</code></p>
  </div>
</div>

<style>
.card-wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1rem;
  margin-bottom: 1.5rem;
}
.card-item {
  border: 1px solid var(--card-border-color, #e9ecef);
  border-radius: 0.5rem;
  padding: 1.25rem;
  background: var(--card-bg, var(--main-bg));
  transition: box-shadow 0.2s;
}
.card-item:hover {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}
.card-item h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
}
.card-item p {
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
}
.card-item code {
  font-size: 0.8rem;
}
</style>
