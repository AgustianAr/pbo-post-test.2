# pbo-post-test.2

KELAS FILM
package com.mycompany.movies.lists;
*Package dari Kelas 'Film'

public final class Film {
*Access Modifier dari Kelas 'Film'.
*'public' berarti package ini dapat diakses dari luar package
*'final' berarti package ini tidak dapat di wariskan lagi ke Kelas lain

private final int id;
private String title;
private String director;
private int year;
*Ini adalah attribut dari kelas Film

public Film(int id, String title, String director, int year) {
*Konstruktor dari pembuatan objek 'Film'

public int getId() {
    return id;
}

public String getTitle() {
    return title;
}

public void setTitle(String title) {
    this.title = title;
}

public String getDirector() {
    return director;
}

public void setDirector(String director) {
    this.director = director;
}

public int getYear() {
    return year;
}

public void setYear(int year) {
    this.year = year;
}
*Pada Bagian ini digunakan untuk mengembalikan nilai dan mengatur nilai dari Attribut Kelas

KELAS MAIN
package com.mycompany.movies;
*package dari kelas 'main'

import com.mycompany.movies.lists.Film;
import java.util.ArrayList;
import java.util.Scanner;
*mengimpor function dari kelas lain dan function utility ArrayList dan Scanner

public final class main {
*Deklarasi Access modifier dari kelas 'main'\

private static final ArrayList<Film> library = new ArrayList<>();
private static final Scanner scanner = new Scanner(System.in);
*membuat Arraylist dari Film yang akan diisi data yang akan dimasukkan dan Scanner untuk membuat sistem Input di Program

int choice;
do {

System.out.println("Library Film - Menu:");
System.out.println("1. Tambah Film");
System.out.println("2. Lihat Daftar Film");
System.out.println("3. Update Film");
System.out.println("4. Hapus Film");
System.out.println("5. Keluar");
choice = scanner.nextInt();
*Sistem Menu dari Program Library Film. menggunakan Input untuk memilih menu dari program

switch (choice) {
    case 1:
        addMovie();
        break;
    case 2:
        viewMovies();
        break;
    case 3:
        updateMovie();
        break;
    case 4:
        deleteMovie();
        break;
    case 5:
        System.out.println("Terima kasih!");
        break;
    default:
        System.out.println("Pilihan tidak valid.");
}

} while (choice != 5);
*Bagian ini memproses Input yang dpilih oleh user pada menu. Program me Run Function sesuai dari Inputan User


private static void addMovie() {
*Function ini digunakan untuk memasukkan Data atau Value film Baru

private static void viewMovies() {
*function ini digunakan untuk melihat Data film yang telah ditambahkan

private static void updateMovie() {
*menambahkan data film yang telah ditambahkan

private static void deleteMovie() {
*menghapus data film yang telah ditambahkan

private static Film findMovieById(int id) {
*mencaari data film dan mereturn nya   
