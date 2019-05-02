# First-Repository
Kalo ada codingan yang salah atau mau dibenerin taro disini dulu, nanti kalo beda topik dibuatin repository yang baru.

contohnya : 
// class control/handler untuk mengeksekusi berbagai algoritma,
// termasuk algoritma untuk membuat objek entity baru
package com.mercubuana.tugasuts;

import java.util.ArrayList;

public class HandlerRutePelayaran {
//	Mendeklarasikan daftarRute yang berjenis array list, 
//	supaya semua data pasien bisa direkam dan ditambahkan kedalam memori.
//	Array list berjenis static supaya bisa diakses tanpa harus membuat objeknya
	public static ArrayList <Pelayaran> daftarRute =
			new ArrayList<Pelayaran>();
	
	
//	method static, yaitu method yang bisa dieksekusi tanpa harus membiat objeknya.
//	method ini akan digunakan untuk merekam data ke dalam memori.
	public static void
	rekamRutePelayaranKeMemori(String kepemilikan, String rincian, int kapasitas,
			int sisa,  char Rute) {
		
//	Membuat objek pelayaranBaru dengan menggunakan data yang dikirim oleh objek boundary
		Pelayaran pelayaranBaru = new Pelayaran(kepemilikan, rincian,
				kapasitas, sisa, Rute);
		
//	Menambahkan objek pelayaranBaru kedalam daftarRute yang berjenis array list
		daftarRute.add(pelayaranBaru);
	}
	
	
//	Method statik untuk membaca data pasien dari memori dan mengembalikannya kepada GUI	
	public static Pelayaran[] bacaDataRutePelayaran() {
		
//		Mendeklarasikan array yang jumlah elemennya sama 
//		dengan jumlah objek didalam array list
		Pelayaran[] arrayPelayaran = new Pelayaran[daftarRute.size()];
		
//		Mengkonversi atau membaca data dari array list 
//		sehingga dapat disimpan dalam array
		arrayPelayaran = daftarRute.toArray(arrayPelayaran);
		
//		Mengembalikan array ke GUI
		return arrayPelayaran;
	}
}
