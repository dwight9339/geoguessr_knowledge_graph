<%*
const country = await tp.system.prompt("Country");
const continent = await tp.system.prompt("Continent");
const filePath = `Places/${continent}/Countries/${country}`;

await tp.file.move(filePath);
%>
---
# 🌍 <%* tR += country %>

## Overview
> A high-level summary of the country's geography, culture, infrastructure, and typical GeoGuessr characteristics.

## Key Metas

- **Language(s):**  
- **Road Markings & Signs:**  
- **Driving Side:**  
- **License Plates:**  
- **Utility Poles & Infrastructure:**  
- **Common Architecture:**  
- **Natural Features:**  

## Continents
- [[<%* tR += continent %>]]

## Subregions
- 

## States/Provinces/Prefectures/Etc
- 

## Major Cities
- 

## Related Concepts
- 

## See Also
- 
