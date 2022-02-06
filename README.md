- 👋 Hi, I’m @KalyanNagaAI
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
KalyanNagaAI/KalyanNagaAI is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
pip install geopy
Requirement already satisfied: geopy in c:\users\kalyan\anaconda3\lib\site-packages (2.2.0)
Requirement already satisfied: geographiclib<2,>=1.49 in c:\users\kalyan\anaconda3\lib\site-packages (from geopy) (1.52)
Note: you may need to restart the kernel to use updated packages.
from geopy.geocoders import Nominatim
geolocator = Nominatim(user_agent="specify_your_app_name_here")
location = geolocator.geocode("175 5th Avenue NYC")
print(location.address)
Flatiron Building, 175, 5th Avenue, Flatiron, New York, NYC, New York, ...
print((location.latitude, location.longitude))
(40.7410861, -73.9896297241625)
print(location.raw)
{'place_id': '9167009604', 'type': 'attraction', ...}
  File "<ipython-input-7-63ca3d48b0fe>", line 5
    Flatiron Building, 175, 5th Avenue, Flatiron, New York, NYC, New York, ...
             ^
SyntaxError: invalid syntax
from geopy.geocoders import Nominatim
geolocator = Nominatim(user_agent="specify_your_app_name_here")
location = geolocator.reverse("52.509669, 13.376294")
print(location.address)
Potsdamer Platz, Mitte, Berlin, 10117, Deutschland, European Union
print((location.latitude, location.longitude))
(52.5094982, 13.3765983)
print(location.raw)
{'place_id': '654513', 'osm_type': 'node', ...}
  File "<ipython-input-8-76543438cbc1>", line 5
    Potsdamer Platz, Mitte, Berlin, 10117, Deutschland, European Union
              ^
SyntaxError: invalid syntax
from geopy.distance import geodesic
newport_ri = (41.49008, -71.312796)
cleveland_oh = (41.499498, -81.695391)
print(geodesic(newport_ri, cleveland_oh).miles)
538.390445368
538.3904453677205
538.390445368
from geopy.distance import great_circle
newport_ri = (41.49008, -71.312796)
cleveland_oh = (41.499498, -81.695391)
print(great_circle(newport_ri, cleveland_oh).miles)
536.997990696
