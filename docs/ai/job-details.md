---
---
# <a name="view-recent-job-performance-and-details"></a>Сведения о недавних заданиях и их производительности

После отправки заданий вы можете просмотреть их список, где указаны их состояние, длительность и многое другое.

1. В окне **Обозреватель сервера** разверните конкретный контекст вычислений.
2. Дважды щелкните **Задания**.
3. Вы увидите список заданий, отправленных в этот вычислительный контекст.
4. Чтобы просмотреть сведения о конкретном **задании**, выберите его в списке.

![Мониторинг заданий](media/job-details/monitor-jobs.png)

> Журнал заданий, отправленных в виртуальные машины Linux, хранится на виртуальной машине в каталоге /tmp. Поэтому при каждой перезагрузке виртуальной машины журнал заданий удаляется. Чтобы он сохранялся, настройте виртуальную машину как контекст вычислений в машинном обучении Azure, а затем отправьте задание в машинное обучение Azure (выбрав виртуальную машину как вычислительный контекст).