# Шпаргалка по командам проверки

## Интерфейсы и L2

| Команда | Что показывает |
|---------|----------------|
| `show ip interface brief` | адреса и состояние (`up/up`) всех интерфейсов |
| `show interfaces <int>` | счётчики ошибок, duplex/speed, MTU |
| `show interfaces status` | краткий статус портов коммутатора |
| `show vlan brief` | VLAN и принадлежность портов |
| `show interfaces trunk` | trunk-порты, allowed и native VLAN |
| `show interfaces <int> switchport` | режим порта (access/trunk), VLAN |
| `show mac address-table` | какие MAC-адреса на каких портах |
| `show cdp neighbors detail` | соседи по CDP: устройство, порт, IP |

## Маршрутизация

| Команда | Что показывает |
|---------|----------------|
| `show ip route` | таблица маршрутизации (`C`, `L`, `S`, `O`) |
| `show ip route <сеть>` | маршрут до конкретной сети |
| `show ip ospf neighbor` | OSPF-соседи и их состояние (`FULL`) |
| `show ip ospf interface brief` | интерфейсы в OSPF, cost, состояние |
| `show ip protocols` | активные протоколы маршрутизации и их сети |
| `show arp` | соответствие IP ↔ MAC |

## Сервисы

| Команда | Что показывает |
|---------|----------------|
| `show ip dhcp binding` | выданные DHCP-адреса |
| `show ip dhcp pool` | статистика пула |
| `show ip nat translations` | активные NAT-трансляции |
| `show ip nat statistics` | счётчики NAT, inside/outside интерфейсы |
| `show access-lists` | ACL и количество срабатываний |

## Конфигурация

| Команда | Что делает |
|---------|-----------|
| `show running-config` | текущая конфигурация |
| `show running-config \| section <слово>` | только нужный раздел |
| `show startup-config` | сохранённая конфигурация |
| `copy running-config startup-config` | сохранить изменения |
| `show version` | версия IOS, время работы, регистр конфигурации |

## Диагностика

| Команда | Что делает |
|---------|-----------|
| `ping <ip>` / `traceroute <ip>` | проверка достижимости и пути |
| `ping <ip> source <интерфейс>` | ping с конкретного интерфейса (проверка маршрута обратно) |
| `debug ip packet` | подробный разбор пакетов (осторожно, нагрузка; отключать: `undebug all`) |
