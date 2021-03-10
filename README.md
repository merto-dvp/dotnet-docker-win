# dotnet-docker-win

Dokümantasyon
Create => Main Project  .NET 5.0 (Proje yeni kuruluyorsa Docker support disabled)

Solution'a; 

Create => dev_v1 (Same Configure)

Create => dev_v2 (Same Configure)

Create => dev_v3 (Same Configure)

Create => dev_v4 (Same Configure)

dev_v1’in içerisine Dockerfile oluşturuldu otomatik olarak.
1. Ana dizinde Common Klasörü oluşturuldu.
- Docker'a ait dosyalar common'a taşındı.
- Main Project'e => Add Docker support 
- Main Project => Add Container Orchestrator Support 
- dev_v1 => Add Docker support 
- dev_v1 => Add Container Orchestrator Support 
- Bunu yaptığımız için Main Project.sln üzerinde docker-compose path'ini Common olarak güncelliyoruz.
2. Docker-compose.override içindekiler, docker-compose içerisine taşınır.
- Portlar editlenir (5000:80 && 5001:80)
- ASPNETCORE_URLS'ten https'ler silinir.(443)
- Startup.cs'e gidilir ve httpsredirection() kapanır.
3. Manuel bir şekilde Docker support vermek;
- Docker-compose içerisinde dev_v1 için olan kısım kopyalanır, sadece dosya pathleri ve port güncellenir. 
- Elle Dockerfile oluşturulur.
- Diğer Dockerfile içerisi kopyalanır ve dev_v2 için elle oluşturduğumuz Dockerfile'e yapıştırılır ve güncellemeler yapılır.
- Docker-compose'a gidilir
-     context : ../    şeklinde güncellenir.
