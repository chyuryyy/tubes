package main
import "fmt"

func main(){
	var budgetTotal, pengeluaranHarian, totalPengeluaran, sisaBudget int
	var i, jumlahHari int
	var daftarPengeluaran []int
	var selesai bool

	fmt.Println("== Aplikasi Pengelolaan Budget Traveling ==")
	fmt.Print("Masukkan total budget: Rp")
	fmt.Scan(&budgetTotal)
	fmt.Print("Masukkan jumlah hari: ")
	fmt.Scan(&jumlahHari)

	for i = 1; i <= jumlahHari; i++ {
		fmt.Printf("Masukkan pengeluaran harian untuk hari ke-%d: Rp", i)
		fmt.Scan(&pengeluaranHarian)
		daftarPengeluaran = append(daftarPengeluaran, pengeluaranHarian)
		totalPengeluaran += pengeluaranHarian
	}

	sisaBudget = budgetTotal - totalPengeluaran

	fmt.Println("\n== Ringkasan Pengeluaran ==")
	fmt.Println("Total budget: Rp", budgetTotal)
	fmt.Println("Jumlah hari: ", jumlahHari)
	fmt.Println("Total pengeluaran: Rp", totalPengeluaran)
	fmt.Println("Sisa budget: Rp", sisaBudget)
	fmt.Println("Daftar pengeluaran harian: ", daftarPengeluaran)

	if sisaBudget > 0 {
		fmt.Printf("Sisa budget Anda sebesar: Rp %d\n", sisaBudget)
	} else {
		fmt.Println("Anda tidak memiliki sisa budget tersisa (Budget Habis).")
		fmt.Println("Terima kasih telah menggunakan aplikasi ini.")
		return
	}

	selesai = false
	for !selesai {
		fmt.Println("\nApakah Anda ingin menambah pengeluaran harian? (Yes/No)")
		var jawab string
		fmt.Print("Jawab: ")
		fmt.Scan(&jawab)

		if jawab == "Yes" {
			var pengeluaranBaru int
			fmt.Print("Masukkan pengeluaran baru: Rp")
			fmt.Scan(&pengeluaranBaru)
			daftarPengeluaran = append(daftarPengeluaran, pengeluaranBaru)
			totalPengeluaran += pengeluaranBaru
			sisaBudget = budgetTotal - totalPengeluaran

			fmt.Println("\n== Ringkasan Pengeluaran Terbaru ==")
			fmt.Println("Total budget: Rp", budgetTotal)
			fmt.Println("Jumlah hari: ", jumlahHari)
			fmt.Println("Total pengeluaran: Rp", totalPengeluaran)
			fmt.Println("Sisa budget: Rp", sisaBudget)
			fmt.Println("Daftar pengeluaran harian: ", daftarPengeluaran)

			if sisaBudget > 0 {
				fmt.Printf("Sisa budget Anda sebesar: Rp %d\n", sisaBudget)
			} else {
				fmt.Println("Anda tidak memiliki sisa budget tersisa (Budget Habis).")
				fmt.Println("Terima kasih telah menggunakan aplikasi ini.")
				selesai = true
			}
		} else if jawab == "No" {
			fmt.Println("Terima kasih telah menggunakan aplikasi ini.")
			selesai = true
		} else {
			fmt.Println("Pilihan tidak valid. Silakan coba lagi.")
		}
	}
}
