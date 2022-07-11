# 45-server-kantoor
<!-- How to start -->
json-server --watch db.json

						Kantoor App
######################################################################################################################

Link Deploy dari BE : https://officebooking-app-pn6n3.ondigitalocean.app

Endpoint : 
######################################################################################################################
<!-- Register User -->
	1. POST -> https://officebooking-app-pn6n3.ondigitalocean.app/register
		Body : {
   			 "email": "ridwan@gmail.com",
    			 "name": "ridwan",
   			 "fullname": "ridwan RAH",
    			 "alamat" : "jl jalan raya",
    			 "phone": "0851222222",
    			 "password": "12345678"
			}

	2. POST -> https://officebooking-app-pn6n3.ondigitalocean.app/login
		Body : {
   			 "email": "ikhsan@gmail.com",
    			 "password": "12345678"
			}

	3. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/users
	4. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/user/:id (contoh = 1)
	5. DELETE -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/users/:id (contoh = 1)
	6. PUT -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/users/:id (contoh = 2)
		Body : {
   			 "name": "judin",
    			 "fullname": "judin fikri",
    			 "email": "judin@gmail.com",
    			 "alamat": "jl raya",
   			 "phone" : "08452723743"
			}

######################################################################################################################
<!-- Manage Gedung  -->
	Admin : 1. POST -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/gedung
			Body : {
    				"name": "The Honey Lady Building",
   				"location": "Jakarta Barat",
    				"price": "450000",
    				"latitude": "-6.2296254",
    				"longitude": "106.8049591",
    				"description": "Sewa Kantor"
				}
	
		2. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/gedungs
		3. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/gedung/:id (contoh = 1)
		4. PUT -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/gedungs/:id (contoh = 1)
			Body : {
    				"name": "The Honey Lady Building",
   				"location": "Jakarta Barat",
    				"price": "450000",
    				"latitude": "-6.2296254",
    				"longitude": "106.8049591",
    				"description": "Sewa Kantor"
				}

		5. DELETE -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/gedung/:id (contoh = 2)
	
	Customer : 1. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/gedung
		   2. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/gedung/price

######################################################################################################################
<!-- Manage Nearby Facilities -->

	Admin : 1. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/nearby
		2. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/nearby/:id (contoh = 1)
		3. POST -> https://officebooking-app-pn6n3.ondigitalocean.app/nearby
			Body : {
    				"namefacilities": "Masjid Nurul Islam",
    				"jenis": "Fasilitas Ibadah",
    				"jarak": "500 M",
    				"latitude": "-6.2300967",
    				"longtitude": "106.8065819"
				}

		4. PUT -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/nearby/:id (contoh = 1)
			Body : {
    				"namefacilities": "Masjid Nurul Islam",
    				"jenis": "Fasilitas Ibadah",
    				"jarak": "500 M",
    				"latitude": "-6.2300967",
    				"longtitude": "106.8065819"
				}
	
	Customer : 1. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/nearby/:id (contoh = 1)
		   2. GET -> https://officebooking-app-pn6n3.ondigitalocean.app/nearby

######################################################################################################################
<!-- Manage Nearby Facilities -->

	Admin : 1. POST -> https://officebooking-app-pn6n3.ondigitalocean.app/review
			Body : {
    				"rating": 5.0, (Harus pakai .0 dibelakang nya)
    				"description": "Fasilitas sangat bagus dan rekomended untuk meeting rame-rame",
				}
	
	Customer : 1. DELETE -> https://officebooking-app-pn6n3.ondigitalocean.app/admin/review/:id (contoh = 1)
