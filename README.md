# Домашнее задание к занятию `«Helm»` - Пугач Евгений.


---

## `Установка Helm`

![Скриншот 1](https://github.com/PugachEV72/Images/blob/master/2024-05-12_16-44-45.png)

---

## `Задание 1. Подготовить Helm-чарт для приложения`

1. Необходимо упаковать приложение в чарт для деплоя в разные окружения.
2. Каждый компонент приложения деплоится отдельным deployment’ом или statefulset’ом.
3. В переменных чарта измените образ приложения для изменения версии.

### Ответ:

Подготовлен чарт:

![Скриншот 2](https://github.com/PugachEV72/Images/blob/master/2024-05-12_17-30-08.png)

В файле Chart.yaml изменена версия app:

![Скриншот 3](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-17-04.png)

[Ссылка на Chart.yaml](https://github.com/PugachEV72/kuber-homeworks-2.5/blob/main/helm/mychart/Chart.yaml)

В файле values.yaml изменена версия nginx и прописаны параметры деплоя multitool:

![Скриншот 4](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-22-41.png)

![Скриншот 5](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-23-56.png)

[Ссылка на values.yaml](https://github.com/PugachEV72/kuber-homeworks-2.5/blob/main/helm/mychart/values.yaml)

В templates/ добавлены deployment и service для multitool:

[Ссылка на deployment-multitool.yaml](https://github.com/PugachEV72/kuber-homeworks-2.5/blob/main/helm/mychart/templates/deployment-multitool.yaml)

[Ссылка на service-multitool.yaml](https://github.com/PugachEV72/kuber-homeworks-2.5/blob/main/helm/mychart/templates/service-multitool.yaml)

---

## `Задание 2. Запустить две версии в разных неймспейсах`

1. Подготовив чарт, необходимо его проверить. Запуститe несколько копий приложения.
2. Одну версию в namespace=app1, вторую версию в том же неймспейсе, третью версию в namespace=app2.
3. Продемонстрируйте результат.

### Ответ:

Нэймспэйс app1: 

![Скриншот 6](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-05-46.png)

![Скриншот 7](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-07-58.png)

Нэймспэйс app2:

![Скриншот 8](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-09-38.png)

![Скриншот 9](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-10-49.png)

---

## `Итог:`

![Скриншот 10](https://github.com/PugachEV72/Images/blob/master/2024-05-12_19-15-59.png)

---


