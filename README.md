### Задание 1

**Что нужно сделать**

Создать Deployment приложения, использующего локальный PV, созданный вручную.

1. Создать Deployment приложения, состоящего из контейнеров busybox и multitool.
2. Создать PV и PVC для подключения папки на локальной ноде, которая будет использована в поде.
<img width="1405" height="227" alt="image" src="https://github.com/user-attachments/assets/92752da0-b653-4d58-ba9e-81be720ce3cb" />
3. Продемонстрировать, что multitool может читать файл, в который busybox пишет каждые пять секунд в общей директории. 
<img width="1494" height="451" alt="image" src="https://github.com/user-attachments/assets/57f4e942-107a-4212-a55c-76b61a53ab0c" />
<img width="1517" height="794" alt="image" src="https://github.com/user-attachments/assets/b3fc8bdc-b678-497b-82a5-2a96d4c2f04d" />

4. Удалить Deployment и PVC. Продемонстрировать, что после этого произошло с PV. Пояснить, почему.
<img width="1372" height="170" alt="image" src="https://github.com/user-attachments/assets/4ecafe8f-bd01-494a-bcef-fdf0cc6086cf" />
Данные сохраняются, так как есть политика повторного использования Retain
5. Продемонстрировать, что файл сохранился на локальном диске ноды. Удалить PV.  Продемонстрировать что произошло с файлом после удаления PV. Пояснить, почему.
<img width="1392" height="807" alt="image" src="https://github.com/user-attachments/assets/cc67652e-991d-4da1-a779-3a9aa4554d6c" />
<img width="1475" height="679" alt="image" src="https://github.com/user-attachments/assets/ada16c42-e114-47a6-99e3-60699d582155" />
Удаление PV в Kubernetes удаляет только объект PersistentVolume из etcd, но не затрагивает фактические данные на диске.
6. Предоставить манифесты, а также скриншоты или вывод необходимых команд.

------

### Задание 2

**Что нужно сделать**

Создать Deployment приложения, которое может хранить файлы на NFS с динамическим созданием PV.

1. Включить и настроить NFS-сервер на MicroK8S.
2. Создать Deployment приложения состоящего из multitool, и подключить к нему PV, созданный автоматически на сервере NFS.
3. Продемонстрировать возможность чтения и записи файла изнутри пода. 
4. Предоставить манифесты, а также скриншоты или вывод необходимых команд.


