< template >
  < div  class = " bayangan kartu mt-3 " >
    < div  class = " badan kartu " >
      < h5  class = " card-title " >Edit teman</ h5 >
      < form  class = " baris g-3 " @ kirim . cegah = " perbarui " >
        < div  class = " col-md-6 " >
          < label  for = " inputEmail4 "  class = " form-label " >Nama</ label >
          < masukan
            ketik = " teks "
            class = " kontrol bentuk "
            id = " inputEmail4 "
            v-model = " teman . nama "
          />
          < div  class = " alert alert-danger "  v-if = " validasi . nama " >
            {{ validasi . nama [ 0 ] }}
          </ div >
        </ div >
        < div  class = " col-md-6 " >
          < label  for = " inputPassword4 "  class = " form-label " >Tanpa Tlp</ label >
          < masukan
            jenis = " nomor "
            class = " kontrol bentuk "
            id = " inputPassword4 "
            v-model = " teman . no_tlp "
          />
          < div  class = " alert alert-danger "  v-if = " validasi . no_tlp " >
            {{ validasi . no_tlp [ 0 ] }}
          </ div >
        </ div >
        < div  class = " col- 6 " >
          < label  for = " inputAddress "  class = " form-label " >Alamat</ label >
          < masukan
            ketik = " teks "

    
        
          
    

        
    
    @@ -40,6 +40,18 @@
  
            class = " kontrol bentuk "
            id = " inputAddress "
            placeholder = " Masukan alamat "
            v-model = " teman . alamat "
          />
          < div  class = " alert alert-danger "  v-if = " validasi . alamat " >
            {{ validasi . alamat [ 0 ] }}
          </ div >
        </ div >
        < div  class = " col-6 " >
          < label  for = " inputAddress "  class = " form-label " >Grup</ label >
          < pilih
            kelas = " bentuk-pilih "
            aria-label = " Contoh pilih default "
            v-model = " teman . groups_id "
          >
            < option  v-for = " group in groups " : key = " group . id " : value = " group . id " >
              {{ kelompok . nama }}
            </ pilihan >
          </ pilih >
        </ div >
        < div  class = " col-12 " >
          < jenis tombol  = " kirim " class = " btn btn-primary " >Edit</ tombol > 
        </ div >

    
        
          
    

        
    
    @@ -48,62 +60,80 @@
  
      </ bentuk >
    </ div >
  </ div >
</ template >
< naskah >
import { onMounted , reaktif , ref } dari " vue " ;  
import { useRoute , useRouter } dari  " vue-router " ;
impor  aksio  dari  " aksios " ;
ekspor  default {
  pengaturan () {
    const  teman  =  reaktif ({
      nama :  " " ,
      no_tlp :  " " ,
      alamat :  " " ,
      group_id :  " "
    });
    biarkan grup =  ref ([]);
     validasi  const =  ref ([]);
    const  router  =  useRouter ();
    const  rute  =  useRoute () ;
    terpasang (() => {
      aksio
        . dapatkan ( ` http://127.0.0.1:8000/api/friends/ ${ route . params . id } /edit ` )
        . lalu (( respon ) => {
          konsol . log ( respon . data . data . nama );
          teman . nama  =  tanggapan . data . data . nama ;
          teman . no_tlp  =  tanggapan . data . data . no_tlp ;
          teman . alamat  =  tanggapan . data . data . alamat ;
          teman . groups_id  =  tanggapan . data . data . grup_id ;
        })
        . tangkap (( kesalahan ) => {
          konsol . log ( error . respon . data );
        });
         aksio
        . dapatkan ( " http://127.0.0.1:8000/api/groups " )
        . lalu (( respon ) => {
          kelompok . nilai  =  respon . data . data ;
          konsol . log (tanggapan);
        })
        . tangkap (( kesalahan ) => {
          konsol . log (kesalahan);
        });
    });
     pembaruan fungsi () {
      biarkan nama =  teman . nama ;
      biarkan no_tlp =  teman . no_tlp ;
      biar alamat =  teman . alamat ;
      biarkan groups_id =  teman . grup_id ;
      aksio
        . put ( ` http://127.0.0.1:8000/api/friends/ ${ route . params . id } ` , {
          nama : nama,
          no_tlp : no_tlp,
          alamat : alamat,
          grup_id : grup_id,
        })
        . lalu (() => {
          router . dorong ({
            nama :  " Rumah " ,
          });
        })
        . tangkap (( kesalahan ) => {
          validasi . nilai  =  kesalahan . respon . data ;
        });
    }
    kembali {
      teman,
      validasi,
      router,
      memperbarui,
      rute,
      kelompok,
    };
  },
};

    
          
            
    

          
    
    
  
</ skrip >