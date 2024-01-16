# NeuralNetworkXOR
Матчасть DL
Задача: реализовать и обучить нейронную сеть, состоящую из 2 нейронов, предсказывать значения функции XOR.
При выполнении лабораторной запрещается использовать фреймворки для глубокого обучения (как PyTorch, Tensorflow, Caffe, Theano и им подобные).
Что необходимо реализовать:

Класс Neuron, имеющий вектор весов self._weigths
Два метода класса Neuron: forward(x), backward(x, loss) - реализующих прямой и обратный проход по нейронной сети. Метод forward должен реализовывать логику работу нейрона: умножение входа на вес self._weigths, сложение и функцию активации сигмоиду. Метод backward должен реализовывать взятие производной от сигмоиды и используя состояние нейрона обновить его веса.
Реализовать с помощью класса Neuron нейронную сеть с архитектурой из трёх нейронов: ![image](https://github.com/ssaabbii/NeuralNetworkXOR/assets/82314846/55fa27d6-a010-41d8-addf-5ed52b396d81)
 



Для красоты обернуть в класс Model с методами forward и backward, реализующими правильное взаимодействие нейронов на прямом и обратном проходах.
Реализовать тренировочный цикл следующего вида:
цикл (обучающие данные):
y = model.forward(x)
err = loss(y, label)
model.backward(x, err)
