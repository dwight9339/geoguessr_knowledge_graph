<%*
const city = await tp.system.prompt("City name");
const country = await tp.system.prompt("Country name");
const continent = await tp.system.prompt("Continent name");
const subdivision = await tp.system.prompt("Subdivision (State/Province/Territory/etc.)");

const folderPath = `Places/${continent}/Countries/${country}/Cities`;
const filePath = `${folderPath}/${city}`;

await tp.file.move(filePath);
%>
# 🏙️ <%* tR += city %>

## Overview
> Population bracket, economic role, layout type (grid vs organic), notable historical or cultural identity.

## Country
- [[<%* tR += country %>]]

## Subdivision (State/Province/Territory/etc.)
- [[<%* tR += subdivision %>]]
## Key Metas
### Languages
- Primary
	- [Primary Language(s)]
- Secondary
	- [Secondary Language(s)]
### Landmarks
- 
### Architecture
- 
### Highways
- 
### Transit
- 

## Related Concepts
- 

## See Also
- 