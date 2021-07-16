<template>
  <div class="card shadow mt-3">
    <div class="card-body">
      <h5 class="card-title">Add friend</h5>
      <form class="row g-3" @submit.prevent="store">
        <div class="col-md-6">
          <label for="inputEmail4" class="form-label">Nama</label>
          <input
            type="text"
            class="form-control"
            id="inputEmail4"
            v-model="friend.nama"
          />
          <div class="alert alert-danger" v-if="validation.nama">
            {{ validation.nama[0] }}
          </div>
        </div>
        < div  class = " col-md-6 " >
          < label  for = " inputPassword4 "  class = " form-label " >Tanpa Tlp</ label >
          < masukan
            jenis = " nomor " 
            class = " kontrol bentuk "
            id = " inputPassword4 "
            v-model = " teman . no_tlp "

    
        
          
    

        
    
    @@ -27,7 +27,7 @@
  
          />
           <div class="alert alert-danger" v-if="validation.no_tlp">
            {{ validasi . no_tlp [ 0 ] }}
          </ div >
        </ div >
        < div  class = " col- 6 " >
          < label  for = " inputAddress "  class = " form-label " >Alamat</ label >
          < masukan
            ketik = " teks "

    
        
          
    

        
    
    @@ -40,6 +40,14 @@
  
            class="form-control"
            id="inputAddress"
            placeholder="masukan alamat"
            v-model="friend.alamat"
          />
           <div class="alert alert-danger" v-if="validation.alamat">
            {{ validasi . alamat [ 0 ] }}
          </ div >
        </ div >
< div  class = " col-6 " >
    < label  for = " inputAddress "  class = " form-label " >Grup</ label >
< pilih  kelas = " form-select "  aria-label = " Contoh pilih default "  v-model = " teman . groups_id " >

  < option  v-for = " group in groups " : key = " group . id " : value = " group . id " >{{ group . nama }}</ opsi >

</ pilih >
</ div >

        < div  class = " col-12 " >
          < jenis tombol  = " kirim " class = " btn btn-primary " >TAMBAHKAN</ tombol > 

    
        
          
    

        
    
    @@ -50,7 +58,7 @@
  
        </div>
      </form>
    </div>
  </div>
</ template >

< naskah >
import { reaktif , ref , onMounted } dari  " vue " ;
impor { useRouter } dari  " vue-router " ;
impor  aksio  dari  " aksios " ;
ekspor  default {

    
        
          
    

        
    
    @@ -59,22 +67,41 @@ ekspor default {
  
  setup() {
    const friend = reactive({
      nama :  " " ,
      no_tlp :  " " ,
      alamat :  " " ,
      group_id :  " "
    });
    biarkan grup =  ref ([]);
     validasi  const =  ref ([]);
    const  router  =  useRouter ();
terpasang (() => {
   aksio
        . dapatkan ( " http://127.0.0.1:8000/api/groups/ " )
        . lalu (( respon ) => {
         kelompok . nilai  =  respon . data ;
          konsol . log (tanggapan);
        })
        . tangkap (( kesalahan ) => {
          
          konsol . log (kesalahan);
        });
});
     penyimpanan fungsi () {
      biarkan nama =  teman . nama ;
      biarkan no_tlp =  teman . no_tlp ;
      biar alamat =  teman . alamat ;
      biarkan groups_id =  teman . grup_id ;
      aksio
        . posting ( " http:// 127.0.0.1:8000 /api/teman/ " , {
          nama : nama,
          no_tlp : no_tlp,
          alamat : alamat,
          groups_id : groups_id
        })
        . lalu (() => {
          router . dorong ({

    
        
          
    

        
    
    @@ -90,6 +117,7 @@ ekspor default {
  
            name: "Home",
          });
        })
        .catch((error) => {
          console.log(error);
        });
    }
    return {
      friend,
      validasi,
      router,
      toko,
      kelompok
    };
  },
};

    
          
            
    

          
    
    
  
</script>