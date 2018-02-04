# Uas_JAva
//arrayLIST
import java.util.ArrayList;
import java.util.Iterator;
import java.util.ListIterator;
import java.util.Arrays;

public class TUGAS_array_list {
    public static void main(String[] args) {
        ArrayList arrayList1;
        arrayList1 = new ArrayList();
        ArrayList arrayList2 = new ArrayList();
        ArrayList<String> names = new ArrayList<String>();
        System.out.println("Dalam Bentuk urutan list horizontal");
        names.add("1.Rektor");
        names.add("3.Dosen");
        names.add("4.Mahasiswa");

        System.out.println("Menampilkan nilai dengan iterator");
        Iterator indivItems = names.iterator();
        while(indivItems.hasNext()){
            System.out.println(indivItems.next());
        }//mengecek iterator apakah mempunyai nilai lanjut atau tidak
        //jika ya maka akan  menampilkan/mengambil nilai selanjutnya
        //intinya sama seperti menampilkan data tetapi iterator akan berhenti jika tidak mempunyai nilai selanjutnya.

        System.out.println("Sesudah ditambahkan");
        names.add(1,"2.Dekan");
        for(int i=0;i<names.size();i++)
        {
            System.out.println(names.get(i));
        }
        System.out.println("Merubah isi ");
        System.out.println("Sebelum Dirubah =");
        for(String i:names)
        {
            System.out.println(i);
        }
        System.out.println("Sesudah dirubah");
        names.set(3 , "4.Mahasiswa Fakultas Teknik");

        for(int i=0;i<names.size();i++)
        {
            System.out.println(names.get(i));
        }
        System.out.println("Dalam Bentuk urutan list vertikal");
        System.out.println(names);


        System.out.println("Menggunakan List Terirator nilai terbalik");
        ListIterator listerator = names.listIterator();
        while(listerator.hasNext()) {
            System.out.println(listerator.next());
        }

        while(listerator.hasPrevious()) {
            System.out.println(listerator.previous());
        }
        //copy dan backup utems
        ArrayList nameCopy = new ArrayList();
        ArrayList nameBackup = new ArrayList();

        //copy items nama
        if (nameCopy.containsAll(names)){
            System.out.println("Semuanya telah dicopy");
        }
        //copied name to namecopy
        //adede to names
        names.clear();
        if(names.isEmpty()){
            System.out.println("Array List Telah Kosong");
        }
        //hapus item nama seluruhnya

        //data telah dibackup
        System.out.println("Menampilkan Data yang dibackup");
        Object[]morenames = new Object[4];
        morenames = nameCopy.toArray();
        System.out.println(Arrays.toString(morenames));

    }
}


