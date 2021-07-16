<template>
  <div class="card shadow mt-3">
    <div class="card-body">
      <h5 class="card-title">Edit friend</h5>
      <form class="row g-3" @submit.prevent="update">
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
        <div class="col-md-6">
          <label for="inputPassword4" class="form-label">No Tlp</label>
          <input
            type="number"
            class="form-control"
            id="inputPassword4"
            v-model="friend.no_tlp"
          />
           <div class="alert alert-danger" v-if="validation.no_tlp">
<template>
  <div class="card shadow mt-3">
    <div class="card-body">
      <h5 class="card-title">Edit friend</h5>
      <form class="row g-3" @submit.prevent="update">
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
        <div class="col-md-6">
          <label for="inputPassword4" class="form-label">No Tlp</label>
          <input
            type="number"
            class="form-control"
            id="inputPassword4"
            v-model="friend.no_tlp"
          />
           <div class="alert alert-danger" v-if="validation.no_tlp">
<template>
  <div class="card shadow mt-3">
    <div class="card-body">
      <h5 class="card-title">Edit friend</h5>
      <form class="row g-3" @submit.prevent="update">
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
        <div class="col-md-6">
          <label for="inputPassword4" class="form-label">No Tlp</label>
          <input
            type="number"
            class="form-control"
            id="inputPassword4"
            v-model="friend.no_tlp"
          />
           <div class="alert alert-danger" v-if="validation.no_tlp">
<template>
  <div class="card shadow mt-3">
    <div class="card-body">
      <h5 class="card-title">Edit friend</h5>
      <form class="row g-3" @submit.prevent="update">
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
        <div class="col-md-6">
          <label for="inputPassword4" class="form-label">No Tlp</label>
          <input
            type="number"
            class="form-control"
            id="inputPassword4"
            v-model="friend.no_tlp"
          />
           <div class="alert alert-danger" v-if="validation.no_tlp">
            {{ validasi . no_tlp [ 0 ] }}
          </ div >
        </ div >
        < div  class = " col- 6 " >
          < label  for = " inputAddress "  class = " form-label " >Alamat</ label >
          < masukan
            ketik = " teks "

    
        
          
    

        
    
    @@ -40,7 +40,14 @@
  
            class="form-control"
            id="inputAddress"
            placeholder="masukan alamat"
            v-model="friend.alamat"
          />
           <div class="alert alert-danger" v-if="validation.alamat">
            class="form-control"
            id="inputAddress"
            placeholder="masukan alamat"
            v-model="friend.alamat"
          />
           <div class="alert alert-danger" v-if="validation.alamat">
            class="form-control"
            id="inputAddress"
            placeholder="masukan alamat"
            v-model="friend.alamat"
          />
           <div class="alert alert-danger" v-if="validation.alamat">
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
          < jenis tombol  = " kirim " class = " btn btn-primary " >Edit</ tombol > 
        </ div >

    
        
          
    

        
    
    @@ -59,36 +66,53 @@ ekspor default {
  
      </form>
    </div>
  </div>
</template>
<script>
import { onMounted, reactive, ref } from "vue";
import { useRouter } from "vue-router";
import axios from "axios";
export default {
  setup() {
    const friend = reactive({
      </form>
    </div>
  </div>
</template>
<script>
import { onMounted, reactive, ref } from "vue";
import { useRouter } from "vue-router";
import axios from "axios";
export default {
  setup() {
    const friend = reactive({
      </form>
    </div>
  </div>
</template>
<script>
import { onMounted, reactive, ref } from "vue";
import { useRouter } from "vue-router";
import axios from "axios";
export default {
  setup() {
    const friend = reactive({
      </form>
    </div>
  </div>
</template>
<script>
import { onMounted, reactive, ref } from "vue";
import { useRouter } from "vue-router";
import axios from "axios";
export default {
  setup() {
    const friend = reactive({
      nama :  " " ,
      no_tlp :  " " ,
      alamat :  " " ,
      group_id :  " " ,
    });
biarkan grup =  ref ([]);
     validasi  const =  ref ([]);
    const  router  =  useRouter ();
    const  rute  =  useRouter ()
    terpasang (() => {
      aksio . dapatkan ( '  http:// 127.0.0.1:8000 /api/friends/${route.params.id} /edit ' )
      . lalu ( respon  => {
        konsol . log ( respon . data . data . nama )
        teman . nama  =  tanggapan . data . data . nama
         teman . no_tlp  =  tanggapan . data . data . no_tlp
          teman . alamat  =  tanggapan . data . data . alamat
           teman . groups_id  =  tanggapan . data . data . grup_id
      }). tangkap ( kesalahan  => {
        konsol . log ( kesalahan . respon . data )
      });
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
     pembaruan fungsi () {
      biarkan nama =  teman . nama ;
      biarkan no_tlp =  teman . no_tlp ;
      biar alamat =  teman . alamat ;
       biarkan groups_id =  teman . grup_id ;
      aksio . put ( ' http:// 127.0.0.1:8000 /api/friends/${route.params.id} ' , {
          nama : nama,
          no_tlp : no_tlp,
          alamat : alamat,
           grup_id : grup_id,
        })
        . lalu (() => {
          router . dorong ({

    
        
          
    

        
    
    @@ -104,7 +128,8 @@ ekspor default {
  
            name: "Home",
          });
        })
        .catch((error) => {
         validation.value = error.response.data
        });
    }
    return {
      friend,
            name: "Home",
          });
        })
        .catch((error) => {
         validation.value = error.response.data
        });
    }
    return {
      friend,
            name: "Home",
          });
        })
        .catch((error) => {
         validation.value = error.response.data
        });
    }
    return {
      friend,
            name: "Home",
          });
        })
        .catch((error) => {
         validation.value = error.response.data
        });
    }
    return {
      friend,
      validasi,
      router,
      memperbarui,
      rute,
      kelompok,
    };
  },
};

    
          
            
    

          
    
    
  
</script>
</script>
</script>
</script>