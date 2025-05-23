<%*
const region = await tp.system.prompt("Region name");
const continent = await tp.system.prompt("Continent");
const targetPath = `Places/${continent}/Regions/${region}`;

await tp.file.move(targetPath);
%>
# 🌐 <%* tR += region %>

**Continent**: [[<%* tR += continent %>]]

## Overview
> _Summary of this region's unifying cultural, historical, geographic, or infrastructural traits._

## Unifying Characteristics
- **Language(s):**
- **Architecture:**
- **Road Signage:**
- **Vegetation/Climate:**
- **Shared History or Culture:**

## Countries
- 

## Related Concepts
- 

## See Also
- 
