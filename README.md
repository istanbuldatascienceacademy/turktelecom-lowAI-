[Net.ServicePointManager]::SecurityProtocol = "Tls12"; Invoke-RestMethod -Method Post -Uri "https://ipke.app.n8n.cloud/webhook-test/ariza" -ContentType "application/json; charset=utf-8" -UseBasicParsing -Body ([Text.Encoding]::UTF8.GetBytes('{"bolge":"Ankara Çankaya","aciklama":"Dünden beri fiber internetim tamamen kesik, modemde LOS ışığı kırmızı yanıyor."}'))


const kayitlar = [
  ["Ankara Çankaya", "Dünden beri fiber internetim tamamen kesik, modemde LOS ışığı kırmızı yanıyor."],
  ["Ankara Kızılay", "Kızılay'daki tüm baz istasyonlarında çekim yok, kimse arama yapamıyor."],
  ["İstanbul Kadıköy", "Faturamda tanımadığım bir 49 TL ücret var."],
  ["İzmir Bornova", "Akşamları internet çok yavaşlıyor, video izleyemiyorum."],
  ["Bursa Nilüfer", "Yeni modemimin kurulumunu yapamadım."],
  ["Antalya Muratpaşa", "Kurumsal hattımızda 3 saattir internet yok, ofis çalışamıyor."],
  ["Eskişehir Tepebaşı", "Fatura son ödeme tarihimi öğrenmek istiyorum."],
  ["Konya Selçuklu", "Evde telefonum hiç çekmiyor, dışarı çıkınca düzeliyor."],
  ["Adana Seyhan", "Modemin wifi şifresini nasıl değiştirebilirim?"],
  ["Trabzon Ortahisar", "Fiber hattım günde birkaç kez kopup geliyor."]
];
return kayitlar.map(([bolge, aciklama]) => ({ json: { body: { bolge, aciklama } } }));
