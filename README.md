application de l'algorithme génétique pour résoudre le problème du voyageur de commerce en utilisant le langage de programmation Python.


- les tableaux x et y représentent les coordonnées des différentes villes.
- num_cities = 15 nombre total de villes dans le problème.
- population_size = 20 :la taille de la population utilisée dans l'algorithme génétique.
chaque individu de la population représente une solution potentielle, c'est-à-dire un chemin qui visite toutes les villes une fois.
- num_iterations = 500 : le nombre d'itérations ou de générations que l'algorithme génétique va parcourir pour améliorer les solutions au fil du temps.
- Pc = 0.8 : représente la probabilité de croisement. Cette valeur indique la probabilité qu'un croisement entre deux individus se produise lors de la génération de la descendance. Dans cet exemple, Pc est défini à 0.8, ce qui signifie qu'il y a une
probabilité de 80% qu'un croisement se produise lors de la création de la nouvelle génération d'individus.
- Pm = 0.1 : représente la probabilité de mutation. Cette valeur indique la probabilité qu'une mutation se produise sur un individu lors de la génération de la descendance. Dans cet exemple, Pm est défini à 0.1, ce qui signifie qu'il y a une probabilité de 10% qu'une mutation se produise sur un individu lors de la création de la nouvelle génération.
Ces paramètres permettent de réguler les opérations de croisement et de mutation dans l'algorithme génétique. Le croisement est utilisé pour échanger les informations génétiques entre les individus afin de créer de nouveaux individus, tandis que la mutation introduit une variation aléatoire dans les individus pour explorer de nouvelles solutions potentielles. Les valeurs de Pc et Pm déterminent l'intensité de ces opérations et peuvent être ajustées pour influencer la diversité et l'exploration de l'espace de recherche de l'algorithme génétique. Les fonctions utilisées dans l'algorithme :
- initialize_population (population_size, num_cities) : cette méthode est responsable de l'initialisation de la population initiale pour l'algorithme génétique. Il génère une population de taille population_size, où chaque individu est une permutation aléatoire de numéros de ville de 0 à num_cities-1.
- calculate_fitness(chemin) : utilise les coordonnées x et y des villes et le chemin spécifié pour calculer la distance totale parcourue lors du parcours des villes dans cet ordre.
- np.sum(np.sqrt(np.sum((xy-np.roll(xy, -1, axis=0))**2, axis=1))) fait la somme de toutes les distances entre les paires de villes, ce qui donne la distance totale parcourue.

- crossover(offspring, parent1, parent2, M, N)) : Cette méthode effectue l'opération de croisement entre deux parents pour produire deux enfants. Un point de croisement est
choisi aléatoirement, puis les parties avant et après ce point sont échangées entre les
parents pour créer deux enfants.
- mutation(offspring,N): Cette méthode effectue l'opération de mutation sur un individu
donné. La mutation consiste à échanger deux villes choisies aléatoirement dans l'ordre
des villes de l'individu. La probabilité de mutation est contrôlée par la variable
mutation_probability










