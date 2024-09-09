# Whatsapp Chat API
Intinya, ini adalah code untuk menghubungkan projek kalian jika ingin melakukan chat whatsapp menggunakan API
[![made-with-javascript](https://img.shields.io/badge/Made%20with-JavaScript-1f425f.svg)](https://www.javascript.com)
[![Npm package version](https://badgen.net/npm/v/express)](https://npmjs.com/package/express)

## Features
- Mengirim Pesan Whatsapp menggunakan API POST / GET






## Installation
kalia bisa download folder atau menggunakan 
```
git clone https://github.com/ipungzz/Whatsapp-API
```

setelah itu kalian buka folder di cmd 
```
cd Whatsapp-Api
npm i
npm start
```
## Cara Penggunaan

Cara penggunaan function
salin kode dibawah ini ke file bakcend kalian
```
function send($nosend,$pesand, $url, $key)
	{
		global $conn;
		$curl = curl_init();
		curl_setopt_array($curl, array(
			CURLOPT_URL => "$url/postapi",
			CURLOPT_RETURNTRANSFER => true,
			CURLOPT_ENCODING => "",
			CURLOPT_MAXREDIRS => 10,
			CURLOPT_TIMEOUT => 30,
			CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
			CURLOPT_CUSTOMREQUEST => "POST",
			CURLOPT_POSTFIELDS => "nomer=$nosend&pesan=$pesand&key=$key",
			CURLOPT_HTTPHEADER => array(
				"cache-control: no-cache",
				"content-type: application/x-www-form-urlencoded"
			),
		));
		curl_exec($curl);

		curl_close($curl);
		return mysqli_affected_rows($conn);

	};
```
untuk memanggil function kalian tinggal salin kode dibawah ini
```
sendwa($nomer,$pesan, $api_url,$key_url);
```

$api_url itu apa sih? jadi itu link buat memanggil project whatsapp, contohnya
```
http://localhost:8080/postapi?
```
Setelah Itu scan qr code menggunakan whatsapp
```
buka whatsapp > titik 3 pojok kanan atas > perangkat tertaut > tautkan perangkat > lalu scan qrcode yang muncul
```


## Dokumentasi
penjelasan lebih jelas, kalian bisa lihat video youtube dibawah ini
[![Drawing-Recognition-Model](https://img.youtube.com/vi/jQ8dZwTw8wQ/0.jpg)](https://www.youtube.com/watch?v=jQ8dZwTw8wQ)
