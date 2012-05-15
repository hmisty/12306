12306
===
12306.cn is well known as the possible world largest online railway ticketing system launched by Ministry Of Railway, China in 2011. It crashed during the 2012 Spring Festival travel season due to the unexpected high load.

This project is a proof-of-concept (PoC) of a large volume high concurrent ticketing system to propose a simple but effective implementation of such a high volume transactional system.

Chunyun
---
[caijing.com.cn] The Spring Festival travel season, or "chunyun," is the world's largest annual migration movement. During the 40-day travel rush, there will be 3.158 billion passenger trips. Among them, 235 million passengers are expected to choose rail as their mode of transportation, indicating that the Ministry of Railways (MOR) will have to allocate at least 235 million tickets during this period.

In early January, China's only official railway ticketing website 12306.cn was overwhelmed with the pressure of more than 1 billion daily visits.

Caijing learned that 12306.cn was originally designed to handle an average daily traffic of only 300 to 400 million passengers for high-speed rail and bullet train online ticket sales.

Traffic reached a peak of 1.4 billion hits in one day, making it "the world's busiest website" and crippling the site¡¯s server in the process. Nevertheless, some improvements have been made since the site launched in early January.

Requirements
---
As reported by caijing.com.cn, we can learn that:
  1. The number of TOTAL railway tickets to be sold was about 235 million. 
  1. The daily visits of 12306.cn was 1.4 billion.

Therefore, this PoC is designed and proven to handle at least:
  1. 500 million transactions per day.
  1. 1.5 billion visits per day.

Moreover, this PoC is designed and proven to be scaled out (almost) linearly, which means:
  1. More capacity can be acquired by simply adding new machines.

Assumptions
---
To simulate the real scenario as much as possible, we need to design extra components:
  1. A simulated SLOW ticketing system which is supposed to be the legacy ticketing system. Ticket bookings need to be synchronized with the legacy system where the consistency is important.
  1. A simulated SLOW payment system which is used for paying the booking.

Technology
---

Architecture
---

Installation
---

Test
---

References
---
  1. Report of 12306.cn by caijing.com.cn http://english.caijing.com.cn/2012-01-31/111649311.html
  1. IBM z/TPF http://www-01.ibm.com/software/htp/tpf/

License
---
This project is published under GPL v3.

12306 - large volume high concurrent ticketing system proof-of-concept

Copyright (C) 2012 Evan Liu (hmisty@gmail.com)

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
