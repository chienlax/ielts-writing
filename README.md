# IELTS Writing Interactive Study Guides

A collection of interactive, responsive study guides, planning templates, and vocabulary toolkits for preparing for the **IELTS Academic Writing Test (Task 1 & Task 2)**. 

These guides are built using a unified modern design system that features responsive sidebars, searchable navigation, color-coded callouts, and layout structures tailored for study and reference.

---

## 📂 Repository Structure

The files are organized into three primary sections: shared styles, Task 1 resources, and Task 2 resources.

### 🎨 Shared Styles & Design System
* **[`style.html`](./style.html)**: The master design template. It details the visual guidelines, typography (featuring *Fraunces* for headers and *Inter* for body text), semantic callout boxes (examples, notes, tips, warnings), data tables, chip groups, and skeleton placeholders used consistently across all other HTML guides.

### 📈 Writing Task 1 (Academic Reports)
* **[`task-1-change-vocab.html`](./task-1-change-vocab.html)**: A vocabulary bank containing structured verb and noun phrasing for trends, fluctuations, rate changes, transitions, and comparison ratios.
* **[`task-1-chart-planning.html`](./task-1-chart-planning.html)**: Structured approaches and steps for planning reports based on line graphs, bar charts, pie charts, and data tables.
* **[`task-1-process-map-planning.html`](./task-1-process-map-planning.html)**: Step-by-step guides for describing process diagrams, cycles, and comparison maps (past vs. present/future).
* **[`task-1-templates.html`](./task-1-templates.html)**: Complete response templates, intro/overview formulas, and paragraph-level structural plans.

### 📝 Writing Task 2 (Academic Essays)
* **[`task-2-argument-guide.html`](./task-2-argument-guide.html)**: A guide for constructing and developing logical arguments, covering Cause & Effect, Contrast & Negation, Counterarguments, and Hedging language.
* **[`task-2-planning-guide.html`](./task-2-planning-guide.html)**: Outlines planning steps and strategies for each Task 2 essay type: Opinion, Discussion, Advantages vs. Disadvantages, Problem & Solution, and Double Questions.
* **[`task-2-templates.html`](./task-2-templates.html)**: Structural templates, paragraph breakdowns, and outline skeletons for drafting Task 2 essays.

---

## 💎 Features of the Guides

* **Sidebar Navigation**: Jump instantly to any section with a sticky side navigation bar that adapts to smaller screen sizes automatically.
* **Semantic Callouts**: Easily distinguish between different types of information:
  * 📘 **Blue (Example)**: Model sentences, paragraphs, and skeleton templates.
  * 📙 **Orange (Key Idea)**: Vital structural principles and core concepts.
  * 🟢 **Green (Tip)**: Writing tips, vocabulary recommendations, and best practices.
  * 🔴 **Red (Warning)**: Common traps, Band-score killers, and pitfalls to avoid.
* **Skeleton Placeholders**: Visual templates showing exactly where to insert specific context, verbs, and nouns in your writing.
* **Responsive Layouts**: Designed to look clean on desktop monitors, tablets, and mobile phones, facilitating self-study anywhere.

---

## 🚀 How to Use

1. **Clone the repository**:
   ```bash
   git clone https://github.com/chienlax/ielts-writing.git
   cd ielts-writing
   ```
2. **Open in Browser**:
   Since these are lightweight, self-contained HTML files, you can double-click or open any file in your favorite web browser (e.g., Chrome, Edge, Safari, Firefox) to start reading and interacting immediately. No local server or build tools are required!

---

## 🛠️ Design Tokens (Customizable)

If you wish to customize the styling theme across the HTML files, you can find the following CSS variables defined in the `<style>` block of each document:

```css
:root {
  --font-display: 'Fraunces', Georgia, serif;
  --font-sans: 'Inter', system-ui, sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
  --bg-page: #fafaf7;          /* Sleek warm-white background */
  --bg-card: #ffffff;
  --text-main: #1a1a1a;
  --text-muted: #555555;
  --border-color: #d8d4c8;
  --accent-primary: #2a5a78;   /* Deep Blue for main accents */
}
```
