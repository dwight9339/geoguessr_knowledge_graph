<%*
const counterPath = app.vault.getAbstractFileByPath("_templates/round_counter.md");
const counterContent = await app.vault.read(counterPath);
let counter = parseInt(counterContent.trim());
const newCounter = counter + 1;

// Update counter file
await app.vault.modify(counterPath, newCounter.toString());

// Format the counter with leading zeros
const paddedCounter = String(counter).padStart(3, "0");
const noteTitle = `round_notes_${paddedCounter}`;
await tp.file.rename(noteTitle);

// Prompt for each field
const language = await tp.system.prompt("Language or script?");
const hemisphere = await tp.system.prompt("Hemisphere (sun position)?");
const drivingSide = await tp.system.prompt("Driving side (left/right)?");
const roadMarkings = await tp.system.prompt("Road markings?");
const architecture = await tp.system.prompt("Architecture style?");
const climate = await tp.system.prompt("Climate/foliage?");
const otherClues = await tp.system.prompt("Other standout clues?");
const guessedLocation = await tp.system.prompt("Your guess (country/region)?");
const reasoningRaw = await tp.system.prompt("Your reasoning (separate with semicolons)");
const actualLocation = await tp.system.prompt("Actual location?");
const coordinates = await tp.system.prompt("Coordinates?");
const distance = await tp.system.prompt("Distance from guess?");
const score = await tp.system.prompt("Score?");
const takeawaysRaw = await tp.system.prompt("Key takeaways (separate with semicolons)");

const reasoning = reasoningRaw.split(";").map(pt => `- ${pt.trim()}`).join("\n");
const takeaways = takeawaysRaw.split(";").map(pt => `- ${pt.trim()}`).join("\n");

tR += `# ${noteTitle}

## 🌐 Observations
**Language/Script:** ${language}  
**Hemisphere (Sun Position):** ${hemisphere}  
**Driving Side:** ${drivingSide}  
**Road Markings:** ${roadMarkings}  
**Architecture Style:** ${architecture}  
**Climate/Foliage:** ${climate}  
**Other Clues:** ${otherClues}  

## 🧠 Initial Guess
**Guessed Location:** ${guessedLocation}  
**Reasoning:**  
${reasoning}

## 📍 Actual Location
**Location:** ${actualLocation}  
**Coordinates:** ${coordinates}  
**Distance from Guess:** ${distance}  
**Score:** ${score}  

## 🧩 Notes & Takeaways
${takeaways}
`;
%>
