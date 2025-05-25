<%*
const name = await tp.system.prompt("Subdivision name");
const country = await tp.system.prompt("Country name");
const continent = await tp.system.prompt("Continent name");
const adminType = await tp.system.prompt("Administrative type (e.g., State, Province, Prefecture)");

const folderPath = `Places/${continent}/Countries/${country}/Subdivisions`;
const filePath = `${folderPath}/${name}`;

await tp.file.move(filePath);
%># 🗺️ <%* tR += name %> (<%* tR += adminType %>)

## Overview
> Summary of this subdivisions’s geography, climate, notable infrastructure, and relevance in GeoGuessr.

## Key Metas
- **Road Markings & Signage:**  
- **Local License Plate Traits:**  
- **Flora & Fauna:**  
- **Common Building Styles:**  
- **Utility Poles & Infrastructure:**  

## Country
- <%* tR += country %>

## Major Cities
- 

## Related Concepts
- 

## See Also
- 
