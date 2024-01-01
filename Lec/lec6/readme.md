Лекция 6 Случайная выборка  
  
Упражнения  
  
Задание 1. Объяснить различие между кодом  
  
    a = np.array([6, 6, 6, 7, 7, 7, 7, 7, 7])  
  
    a[np.random.randint(len(a), size=5)]  
  
и кодом  
  
    np.random.randint(6, 8, 5)  
  
Задание 2. В примере 2 использовался метод np.random.random_integers для выборки из равномерного распределения по числам с плавающей точкой [1/2, 3/2, 5/2, 7/2]. Как можно сделать то же самое, воспользовавшись методом np.random.randint?  
  
    import numpy as np  
  
    a = np.random.uniform(0,1,5)  
    print(a)  
    import numpy as np  
    a = np.random.uniform(0,1,5)  
    print(a)  
  
Задание 3. Американская лотерея Mega Millions во время написания этой книги использовала выбор 5 чисел из 70 и одного из 25. Джекпот распределяется между игроками, выбравшими номера, совпадающие со случайно выбранными. Какова вероятность выиграть джекпот? Написать однострочный код Python, используя библиотеку NumPy, для выбора набора случайных чисел для игрока.  
  
    import numpy as np  
  
    a = np.concatenate((np.random.choice(70,5,replace=False),np.random.choice(25,1)))  
  
    print(a)  