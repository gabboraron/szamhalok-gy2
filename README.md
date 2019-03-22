# gy3

## Shell programok hívása Pythonból
paraméterezve hívja a `ping` utasítást, `5`ször fut le a `google.com`-ra: 
````Python
import subprocess

p = subprocess.Popen(["ping","-c",  "5", "google.com"], stdout= subprocess.PIPE)
print(p.communicate())
````
## JSON kezelés
**bővítés:**
````Python
import json

json_string= """
{
	"researcher": {
		"name": "Ford Prefect",
		"species": "Betelgeusian",
		"relatives": [
			{
				"name": "Zaphod Beeblebrox",
				"species": "Betelgeusian"
			}
		]
	}
}
"""
data = json.loads(json_string)
test = json.dumps(data)
print(test)

data['researcher']['relatives'].append(({'a': 'aaaa', 'b': 'aaaa', 'c': 'aaaa'}))
test = json.dumps(data)
print(test)
````
## Parancssori argumentumok
bővebben: 
https://www.pythonforbeginners.com/system/python-sys-argv
````Python
import sys
print "given arguments: ", str(sys.argv[1])
````
## Hálózat
### `ping`
`ttl` - time to live: 64es értékről indul ha 0zódik akkor az elveszett
    - a ttl az azon eszközök száma amin átmegy a csomag a célig

### `tracert` és `traceroute`
- hbone.hu - magyarországi gerinchálózat
- telia.net - nemzetközi hálózat
- `*`  - nem adja vissza, hogy ki ő

## Hozzá tartozó házi:
> hf1: https://github.com/gabboraron/szamhalok-hf1-hf2#feladat1
