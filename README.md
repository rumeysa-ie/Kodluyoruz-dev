# Kodluyoruz-dev

import math
def euclideanDistance(point1, point2):
  """
  Bu fonksiyon, iki nokta arasındaki Öklid mesafesini hesaplar.

  Args:
    point1: Bir demet (x1, y1) olarak verilen ilk nokta.
    point2: Bir demet (x2, y2) olarak verilen ikinci nokta.

  Returns:
    İki nokta arasındaki Öklid mesafesi.
  """
  x1, y1 = point1
  x2, y2 = point2
  return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)

points = [(1, 1), (2, 2), (3, 1), (4, 3)]

distances = []

for i in range(len(points)):
  for j in range(i + 1, len(points)):
    distance = euclideanDistance(points[i], points[j])
    distances.append(distance)

minimum_distance = min(distances)
print("Minimum mesafe:", minimum_distance, "metre")
