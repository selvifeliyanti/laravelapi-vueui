< template >
  < div  class = " card text-center mt-4 "  v-for = " f in friend " : key = " f . id " >
  < div  class = " card-header " >
    Detail teman
  </ div >
  < div  class = " badan kartu " >
    < h5  class = " judul kartu " >{{ f . nama }}</ h5 >
    < p  class = " kartu-teks " >{{ f . no_tlp }}</ p >
    < p  class = " kartu-teks " >{{ f . alamat }}</ p >
     < p  class = " kartu-teks " >{{ f . kelompok . nama }}</ p >

  </ div >
  < div  class = " footer kartu " >
  < router-link  class = " btn btn-success " : to = " {name :  ' Editfriends ' , params : {id : f . id }} "
              >Edit</ router-link
            >
            < tombol @ klik . Mencegah = " friendDelete ( f . id ) "   class = " btn btn-bahaya " > menghapus </ button >
  </ div >
</ div >
</ template >

< naskah >
import { onMounted ,   ref } dari  " vue " ;
impor { useRouter } dari  " vue-router " ;
impor  aksio  dari  " aksios " ;
ekspor  default {
  pengaturan () {
   
   biarkan teman =  ref ([]);
    const  router  =  useRouter ();
 validasi  const =  ref ([]);
    const  rute  =  useRouter ();
    terpasang (() => {
      aksio . dapatkan ( ' http://127.0.0.1:8000/api/friends/${route.params.id} ' )
      . lalu ( respon  => {
        konsol . log ( respon . data . data . nama )
        teman . nilai  =  respon . data . data . nama
        
      }). tangkap ( kesalahan  => {
        konsol . log ( kesalahan . respon . data )
      });
    });
     fungsi  temanHapus ( id ){
    aksio . hapus ( ` http://127.0.0.1:8000/api/friends/ ${ id } ` )
    . lalu (() => {
      router . pergi ( - 1 );
    }). tangkap ( kesalahan  => {
      konsol . log (kesalahan)
    });
  }
    
    
    kembali {
      teman,
      validasi,
      router,
      temanHapus, 
      rute,
     
    };
  },
};
</ skrip >

< gaya >
</ gaya 