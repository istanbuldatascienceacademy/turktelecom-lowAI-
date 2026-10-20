$body = @{ bolge = "Ankara Çankaya"; aciklama = "Dünden beri fiber internetim tamamen kesik, modemde LOS ışığı kırmızı yanıyor." } | ConvertTo-Json
Invoke-RestMethod -Uri "http://localhost:5678/webhook-test/ariza" -Method Post -ContentType "application/json; charset=utf-8" -Body ([System.Text.Encoding]::UTF8.GetBytes($body))
