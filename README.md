# Ujian Akhir Semester
<br>Mata Kuliah 	: Dasar Pemograman
<br> Nama		: FADLIL YANI AINI SYAMSI
<br>NIM		:	1227050041
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
Tema utama dari source code yang satu ini adalah untuk membuat array dalam implementasi deret aritmatika.<br>
Tujuan utama dari source code ini adalah untuk mencari bilangan yang tidak habis dibagi angka 3,5 dan 7</br>
Algoritma dari Source code ini yaitu : <br>
<ol>
<li>User menginputkan berapa banyak baris pada array mulai dari range 0-20.</li>
<li>User menginputkan berapa banyak baris pada array mulai dari range 0-20.</li>
<li>User menginputkan satu persatu nilai array,dimulai dari baris 1 dan kolom 1.</li>
<li>Jika sudah,Nilai dalam array tersebut di tampilkan sesuai aturan matriks.</li>
<li>Kemudian nilai divalidasi kembali apakah nilai tersebut habis dibagi 3,5 dan 7.</li>
<li>Apabila nilai tadi habis dibagi 3,5 dan 7, maka nilai tidak akan ditampilkan. apabila tidak habis. tampilkan kembali kepada user</li>
</ol>

## Source Code
<code>
#include <iostream>

using namespace std;

void garis(){
	cout<<"---------------------"<<endl;
}

main(){
	int br,kl,x,y,z,i;
	cout<<"Inputkan berapa banyak baris yang diinginkan untuk array : ";
	baris:
	cin>>br;
	if(br>20){
		cout<<"Baris anda terlalu banyak!!"<<endl;
		goto baris;
	}
	cout<<"Inputkan berapa banyak kolom yang diinginkan untuk array : ";
	cin>>kl;
	if(kl>20){
		cout<<"Kolom anda terlalu banyak!!"<<endl;
		goto baris;
	}
	garis();
	
	int array[br][kl];
    cout<<"Berikan nilai pada array!"<<endl;
    garis();
    for (x=1; x<=br; x++){
    	for(y=1; y<=kl; y++){
    		cout<<"Array baris ke-"<<x<<" kolom ke-"<<y<<": \n";
    		cin>>array[x][y];
		}
		garis();
	}	
	
	cout<<"Array awal : \n";
	garis();
	for(x=1;x<=br;x++){
		for(y=1;y<=kl;y++){
				cout<<" "<<array[x][y];
		}
		cout<<endl;
	}
	garis();
	
	int hasil[x * y];
	int kali=0;
	for(x=1;x<=br;x++){
		for(y=1;y<=kl;y++){
			if(array[x][y]%3 != 0 && array[x][y]%5 != 0 && array[x][y]%7 != 0){
				hasil[kali]=array[x][y];
				kali++;
			}
		}
	}
	
	cout<<"\nHasilnya yang tidak bisa dibagi 3, 5, 7 adalah : ";
	for(int i = 0; i < kali; i++){
		cout<<hasil[i];
		if(i < kali -1){
			cout<<", ";
		}else{
			cout<<".";
		}
	}
}
</code>

## Output
  ![Output UAS 2](https://user-images.githubusercontent.com/113232952/209471315-f6ee809b-2bf8-48c8-b5dc-c871369c157d.png)
