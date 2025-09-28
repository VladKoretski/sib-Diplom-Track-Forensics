# Дипломная работа по профессии «Специалист по информационной безопасности». Track Forensics

### Корецкий Владимир Павлович  

### Описание инцидента
Службой безопасности компании «Х» была зафиксирована подозрительная сетевая активность. Вам нужно проанализировать ситуацию, расследовать инцидент и найти следы активности атакующих.
[Исходные данные](https://disk.yandex.ru/d/cYI1nU_Uy4mfAg):  
* дамп оперативной памяти;  
* побитовая копия диска.  

### Общая информация о представленных данных (evidencies)  
#### Dump оперативной памяти 
* Файл - incident.mem (дамп оперативной памяти)  
* Type файла: MEM  
* Verification  MD5: 3defe10c68be87df7c5bc94edc1113cf  
* Verification SHA1: 63a6a6d761231e894852b142b4e31d2aee87d1d0  
* Unique Description: Wilfred Wood's Memory Dump    

PS C:\Users\vladk\Desktop\FinalWorkSecurity\DumpRAMforensic\Tools> .\volatility_2.6_win64_standalone.exe -f "C:\Users\vladk\Desktop\FinalWorkSecurity\FinalWorkTrackForensics\Incident.mem" imageinfo
Volatility Foundation Volatility Framework 2.6
INFO    : volatility.debug    : Determining profile based on KDBG search...
          Suggested Profile(s) : Win7SP1x86_23418, Win7SP0x86, Win7SP1x86
                     AS Layer1 : IA32PagedMemoryPae (Kernel AS)
                     AS Layer2 : FileAddressSpace (C:\Users\vladk\Desktop\FinalWorkSecurity\FinalWorkTrackForensics\Incident.mem)
                      PAE type : PAE
                           DTB : 0x185000L
                          KDBG : 0x82745de8L
          Number of Processors : 1
     Image Type (Service Pack) : 1
                KPCR for CPU 0 : 0x80b96000L
             KUSER_SHARED_DATA : 0xffdf0000L
           Image date and time : 2019-03-10 13:06:28 UTC+0000
     Image local date and time : 2019-03-10 06:06:28 -0700

  
#### Dump жесткого диска - побитовая копия диска  
* Файл - Wood.E01 (побитовая копия диска)  
* Type файла: E01  
* Verification MD5: 84648ad119e390f8cf2201a145c5d8ba  
* Verification SHA1: 0e52068110899a5279eeb7617fb7ace089fde135 
* Unique Description: Wilfred Wood's PC  
  
### Задача
Составить подробный отчёт о проведённом расследовании. Он должен включать себя информацию, подкреплённую доказательствами в виде скриншотов:
* обнаруженные следы атакующих;
* восстановление картины произошедшего инцидента в виде описания характеристики инцидента;
* маппинг действий атакующих по матрице MITRE ATT&CK;
* предложения по ликвидации последствий и восстановлению.

### Пример структуры отчёта
  1.    Характеристика инцидента.    
  2.    Описание инцидента по матрице MITRE ATT&CK.    
    2.1.    Первоначальное проникновение (Initial Access).    
    2.2.    ***************    
    2.3.    ***************    
    2.\*.    ***************    
    2.\*.    ***************    
  3. Рекомендации по ликвидации последствий инцидента и восстановлению.   

### Виды документов для отчёта
1. Характеристика инцидента — в виде текстового пояснения, описывающего ход инцидента, а также отражать действия атакующих на каждом из этапов без технических подробностей.
2. Маппинг действий атакующих по матрице MITRE ATT&CK — в виде таблицы, отражающей соответствие тактики и техник, которые использовали атакующие в рамках исследуемого инцидента.

Описание каждого из этапов инцидента по матрице MITRE ATT&CK нужно оформить в формате:
* указать технику;
* дать описание действиям атакующих и выполненным процедурам;
* подкрепить выводы скриншотами.

В конце отчёта в рамках дополнительного задания можно дать рекомендации по ликвидации последствий инцидента и восстановлению.
