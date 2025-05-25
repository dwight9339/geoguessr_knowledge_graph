<%*
const name = await tp.system.prompt("Subregion name");
const country = await tp.system.prompt("Country name");
const continent = await tp.system.prompt("Continent name");

const folderPath = `Places/${continent}/Countries/${country}/Regions`;
const filePath = `${folderPath}/${name}`;

await tp.file.move(filePath);
%>
# 🗺️ <%* tR += name %>

## Overview
> Broad description of this subregion's geographic range, cultural or environmental unity, and significance for GeoGuessr.

## Country
- [[<%* tR += country %>]]

## Subdivisions (States/Provinces/Territories/etc.)
- 

## Key Metas
- **Typical road features:**  
- **Flora/Fauna/Soil colors:**  
- **License plate subtleties (if any):**  
- **Street layout or signage patterns:**  

## Related Concepts
- 

## See Also
- 
