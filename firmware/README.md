# Бинарные прошивки для FBG6

## Прошивки Klipper для MKS Robin Nano V3, Nano4 (FBG6), Nano6(Reborn)
Прошивки скомпилированы под соответствующие интерфейсы связи:

[USB (PA11/PA12)](
https://github.com/evgs/FBG6-Klipper/raw/main/firmware/klipper-v0.11.0-198/mks-robin-nano-v3-usb/firmware.bin) - разъём USB-B на лицевой панели принтера

[USART1 (PA10/PA9)](
https://github.com/evgs/FBG6-Klipper/raw/main/firmware/klipper-v0.11.0-198/mks-robin-nano-v3-usart1/firmware.bin) - контакты RX1/TX1 на панельке модуля WiFi (сам модуль извлечь)

[USART3 (PB11/PB10)](
https://github.com/evgs/FBG6-Klipper/raw/main/firmware/klipper-v0.11.0-198/mks-robin-nano-v3-usart1/firmware.bin) - контакты RX3/TX3 рядом с панелькой модуля WiFi


Скачать файл `firmware.bin`, записать на карту microSD (формат FAT32), установить карту в принтер, перезагрузить. Подождать пару минут, выключить принтер, извлечь карту.

В случае успешной прошивки файл будет переименован `FIRMWARE.CUR`

## Оригинальный загрузчик MKS Robin Nano4

[Загрузчик](
https://github.com/evgs/FBG6-Klipper/raw/main/firmware/bldr_mksnano4v3.1.bin) считан с платы принтера первой ревизии, выпуск - лето 2022г. От загрузчика MKS Robin Nano V3.1 отличается именем ожидаемого файла прошивки - `ROBIN_NANO_4.BIN`, либо `FIRMWARE.BIN`

Для записи загрузчика в чистый процессор без программатора можно задействовать режим DFU:
1. Замкнуть перемычку BOOT на плате
2. Замкнуть перемычку USB_PWR для питания платы от USB
3. Подключить плату к компьютеру кабелем USB
4. воспользоваться программами STM32CubeProg (Windows), либо dfu-util (Linux, MAC)

Кстати, dfu-util автоматически устанавливается в составе Klipper
