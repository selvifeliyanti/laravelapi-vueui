< template >
< div  kelas = " baris " >
  < div 
  kelas = " col-lg-4 mt-3 " 
  v-for = " (teman, indeks) di teman " 
  : kunci = " indeks "
  >
  < kelas div  = " kartu " >
  < div  class = " card-header " > {{ teman . nama }}
  </ div >
  < div  class = " badan kartu " >
    < h5  class = " judul kartu " >{{ teman . no_tlp }}</ h5 >
    < p  class = " kartu-teks " >{{ teman . alamat }}</ p >
     < p  class = " kartu-teks " >{{ teman . kelompok . nama }}</ p >

  </ div >
< div  class = " card-footer text-muted " >
   < router-link  class = " btn btn-primary " : to = " {name :  ' Detailfriends ' , params : {id : friend . id }} "
              >Edit</ router-link
            >
</ div >
</ div >
</ div >
</ div >
</ template >

< naskah >
ekspor  default {
    alat peraga : [ " teman " ],
};
</ skrip >

< gaya >
</ gaya >