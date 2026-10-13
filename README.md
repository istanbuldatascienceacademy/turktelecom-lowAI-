# turktelecom-lowAI-

[Net.ServicePointManager]::SecurityProtocol = "Tls12"; $veri = @{ bolge = "Ankara Çankaya"; aciklama = "Fiber internetim tamamen kesik, modemde LOS ışığı kırmızı yanıyor." }; $json = $veri | ConvertTo-Json; $istek = @{ Uri = "https://ipke.app.n8n.cloud/webhook-test/ariza"; Method = "Post"; ContentType = "application/json; charset=utf-8"; Body = [Text.Encoding]::UTF8.GetBytes($json) }; Invoke-RestMethod @istek -UseBasicParsing
