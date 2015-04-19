# Nasabah_Bank
Sistem informasi nasabah bank
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package nasabah_bank;

/**
 *
 * @author Asus X452E
 */
public class Alamat {
    private String jalan;
    private String kota;
    private String prov;
    private String kab;
    private String kec;

    /**
     * @return the jalan
     */
    public String getJalan() {
        return jalan;
    }

    /**
     * @param jalan the jalan to set
     */
    public void setJalan(String jalan) {
        this.jalan = jalan;
    }

    /**
     * @return the kota
     */
    public String getKota() {
        return kota;
    }

    /**
     * @param kota the kota to set
     */
    public void setKota(String kota) {
        this.kota = kota;
    }

    /**
     * @return the prov
     */
    public String getProv() {
        return prov;
    }

    /**
     * @param prov the prov to set
     */
    public void setProv(String prov) {
        this.prov = prov;
    }

    /**
     * @return the kab
     */
    public String getKab() {
        return kab;
    }

    /**
     * @param kab the kab to set
     */
    public void setKab(String kab) {
        this.kab = kab;
    }

    /**
     * @return the kec
     */
    public String getKec() {
        return kec;
    }

    /**
     * @param kec the kec to set
     */
    public void setKec(String kec) {
        this.kec = kec;
    }
    
}

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package nasabah_bank;

/**
 *
 * @author Asus X452E
 */
public class Bank {
    private String nama;
    private String cabang;
    private String kode;

    /**
     * @return the nama
     */
    public String getNama() {
        return nama;
    }

    /**
     * @param nama the nama to set
     */
    public void setNama(String nama) {
        this.nama = nama;
    }

    /**
     * @return the cabang
     */
    public String getCabang() {
        return cabang;
    }

    /**
     * @param cabang the cabang to set
     */
    public void setCabang(String cabang) {
        this.cabang = cabang;
    }

    /**
     * @return the kode
     */
    public String getKode()throws Exception {
        try{
        if(!nama.isEmpty()){
            if(nama.equals("BRI"))return "002";
            else if(nama.equals("Mandiri"))return "008";
            else if(nama.equals("BCA"))return "014";
            else if(nama.equals("BNI"))return "009";
            else if(nama.equals("Alfindo"))return "503";
            else if(nama.equals("BII"))return "016";
            else if(nama.equals("Bukopin"))return "441";
            else if(nama.equals("Danamon"))return "011";
            else if(nama.equals("DKI"))return "111";
            else {return "belum terdaftar";}
            
        }
        }catch (Exception e){throw new Exception ("masukan nama Bank");}
        return "";
        
    }

    /**
     * @param kode the kode to set
     */
   
    
}

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package nasabah_bank;

/**
 *
 * @author Asus X452E
 */
public class KTP {
    private String nama;
    private String ttl;
    private String jk;
    private Alamat alamat;
    private String agama;
    private String statusPerkawinan;
    private String pekerjaan;
    private String kewarganegaraan;
    private String tglBerlaku;
    Tanggal tanggal;

    /**
     * @return the nama
     */
    public String getNama() {
        return nama;
    }

    /**
     * @param nama the nama to set
     */
    public void setNama(String nama) {
        for(int i=0; i<nama.length(); i++){
            if(Character.isDigit(nama.charAt(i))){return;}
        }this.nama=nama;
    }

    /**
     * @return the ttl
     */
    public String getTtl() {
        return ttl;
    }

    /**
     * @param ttl the ttl to set
     */
    public void setTtl(String tempat, String tgl, String bulan, String tahun) {
        tanggal=new Tanggal();
        tanggal.setTgl(tgl);
        tanggal.setBulan(bulan);
        tanggal.setTahun(tahun);
        
    }

    /**
     * @return the jk
     */
    public String getJk() {
        return jk;
    }

    /**
     * @param jk the jk to set
     */
    public void setJk(String jk) {
        this.jk = jk;
    }

    /**
     * @return the alamat
     */
    public String getAlamat() {
       return alamat.getJalan()+","+alamat.getKota()+","+alamat.getKec()+","+alamat.getKab()+","+alamat.getProv();
    }

    /**
     * @param alamat the alamat to set
     */
    public void setAlamat(String jalan, String kota, String kab, String prov, String kec) {
        alamat=new Alamat();
        alamat.setJalan(jalan);
        alamat.setKota(kota);
        alamat.setKab(kab);
        alamat.setProv(prov);
        alamat.setKec(kec);
        
    }
    

    /**
     * @return the agama
     */
    public String getAgama() {
        return agama;
    }

    /**
     * @param agama the agama to set
     */
    public void setAgama(String agama) {
        this.agama = agama;
    }

    /**
     * @return the statusPerkawinan
     */
    public String getStatusPerkawinan() {
        return statusPerkawinan;
    }

    /**
     * @param statusPerkawinan the statusPerkawinan to set
     */
    public void setStatusPerkawinan(String statusPerkawinan) {
        this.statusPerkawinan = statusPerkawinan;
    }

    /**
     * @return the pekerjaan
     */
    public String getPekerjaan() {
        return pekerjaan;
    }

    /**
     * @param pekerjaan the pekerjaan to set
     */
    public void setPekerjaan(String pekerjaan) {
        this.pekerjaan = pekerjaan;
    }

    /**
     * @return the kewarganegaraan
     */
    public String getKewarganegaraan() {
        return kewarganegaraan;
    }

    /**
     * @param kewarganegaraan the kewarganegaraan to set
     */
    public void setKewarganegaraan(String kewarganegaraan) {
        this.kewarganegaraan = kewarganegaraan;
    }

    /**
     * @return the tglBerlaku
     */
    public String getTglBerlaku() {
        return tanggal.getTgl()+"-"+tanggal.getBulan()+"-"+tanggal.getTahun();
    }

    /**
     * @param tglBerlaku the tglBerlaku to set
     */
    public void setTglBerlaku(String tgl, String bulan, String tahun) {
        tanggal=new Tanggal();
        tanggal.setTgl(tgl);
        tanggal.setBulan(bulan);
        tanggal.setTahun(tahun);
    }
    
    
}

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package nasabah_bank;

import java.util.logging.Level;
import java.util.logging.Logger;

/**
 *
 * @author Asus X452E
 */
public class Nasabah {
    private String nama;
    private String agama;
    private String alamat;
    private String noRekening;
    private Bank bank;
    private String noHp;
    private KTP ktp;
    private double jmlUang;
   
    

    /**
     * @return the nama
     */
    public void setNasabah(KTP ktp, String noRekening, double jmlUang, String noHp, String nama_Bank, String nama_cabang)throws Exception{
        setNama(ktp.getNama());
        setAgama(ktp.getAgama());
        setAlamat(ktp.getAlamat());
        setJmlUang_awal(jmlUang);
        try {
            setNoRekening(noRekening);
        } catch (Exception ex) {
            throw new Exception (ex.getMessage());
        }
        
        try {
            setNoHp(noHp);
        } catch (Exception ex) {
            throw new Exception (ex.getMessage());
        }

        setBank(nama_Bank, nama_cabang);
    
    }
    
    public String getNama() {
        return nama;
    }

    /**
     * @param nama the nama to set
     */
    private void setNama(String nama) {
        for(int i=0; i<nama.length(); i++){
            if(Character.isDigit(nama.charAt(i))){return;}
        }this.nama=nama;
    }

    /**
     * @return the alamat
     */
    public String getAlamat() {
        return alamat;
    }

    /**
     * @param alamat the alamat to set
     */
    private void setAlamat(String alamat) {
        
        this.alamat=alamat;
        
    }

    /**
     * @return the noRekening
     */
    public String getNoRekening() {
        return noRekening;
    }

    /**
     * @param noRekening the noRekening to set
     */
    private void setNoRekening(String noRekening)throws Exception {
        try{
            Integer.parseInt(noRekening);  
        }catch(Exception e){  
            throw new Exception ("No Rekening harus berupa angka");
        }
        this.noRekening = noRekening;
    }

    /**
     * @return the bank
     */
    public String getBank()throws Exception {
        try {
            return bank.getNama()+" kode: "+bank.getKode();
        } catch (Exception ex) {
            throw new Exception (ex.getMessage());
        }
    }
    
    public  String getNamaBank(){
        return bank.getNama();
    }

    /**
     * @param bank the bank to set
     */
    private void setBank(String namaBank, String cabang) {
        bank=new Bank();
        bank.setNama(namaBank);
        bank.setCabang(cabang);
    }

    /**
     * @return the noHp
     */
    public String getNoHp() {
        return noHp;
    }

    /**
     * @param noHp the noHp to set
     */
    public void setNoHp(String noHp)throws Exception {
        try{
            Integer.parseInt(noHp);  
        }catch(Exception e){  
            throw new Exception ("No Hp harus berupa angka");
        }
        
        this.noHp = noHp;
    }
    
    public void setAgama(String agama){
        this.agama=agama;
    }
    public String getAgama(){
        return agama;
    }
    
    private void setJmlUang_awal(double jmlhUang){
        this.jmlUang=jmlhUang;
    }
    public double getJmlUang(){
        return jmlUang;
    }
    
    public void penambahanUang(Transaksi simpan){
        
        this.jmlUang  =this.jmlUang + simpan.getJmlUang();
    }
    public void penarikan(Transaksi tarik){
        
        this.jmlUang  = this.jmlUang - tarik.getJmlUang();
    }
    public void pengiriman(Transaksi kirim){
        this.jmlUang  = this.jmlUang - kirim.getJmlUang();
    }
      
}

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package nasabah_bank;

/**
 *
 * @author Asus X452E
 */
public class Tanggal {
    private String tgl;
    private String bulan;
    private String tahun;
    
    /**
     * @return the tgl
     */
    public String getTgl() {
        return tgl;
    }

    /**
     * @param tgl the tgl to set
     */
    public void setTgl(String tgl) {
        this.tgl = tgl;
    }

    /**
     * @return the bulan
     */
    public String getBulan() {
        return bulan;
    }

    /**
     * @param bulan the bulan to set
     */
    public void setBulan(String bulan) {
        this.bulan = bulan;
    }

    /**
     * @return the tahun
     */
    public String getTahun() {
        return tahun;
    }

    /**
     * @param tahun the tahun to set
     */
    public void setTahun(String tahun) {
        this.tahun = tahun;
    }
    
    
    
    
}


/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package nasabah_bank;


/**
 *
 * @author Asus X452E
 */
public class Transaksi {
    
    private Nasabah nasabah;
    private double jmlUang;
    private String noRekening;
    private Tanggal tanggal;
    
    public void simpanUang(Nasabah nasabah, double jumlahUang)throws Exception{
        
        setNorekening(nasabah);
        try {
            setJmlUang(jumlahUang);
        } catch (Exception ex) {
            throw new Exception (ex.getMessage());
        }

        nasabah.penambahanUang(this);
    }
    
    public void tarikUang(Nasabah nasabah, double jumlahUang)throws Exception{
        
        setNorekening(nasabah);
        try {
            setJmlUang(jumlahUang);
        } catch (Exception ex) {throw new Exception (ex.getMessage());
        }
        
        try {
            if(nasabah.getJmlUang() > jumlahUang){
                nasabah.penarikan(this);}
            else{throw new Exception("saldo tidak mencukupi");}
        }catch (Exception ex){throw new Exception(": "+nasabah.getNama()+", saldo tidak mencukupi");}
    }
    
    public void kirimUang(Nasabah nasabah, Nasabah nasabah_tujuan, double jumlahUang)throws Exception{
        
        setNorekening(nasabah);
        try {
            setJmlUang(jumlahUang);
        } catch (Exception ex) {throw new Exception (ex.getMessage());
        }
        
        try {
            if(nasabah.getJmlUang() > jumlahUang){
                nasabah.pengiriman(this);
                simpanUang(nasabah_tujuan, jumlahUang);
            }
            else{throw new Exception("saldo tidak mencukupi");}
        }catch (Exception ex){throw new Exception(": "+nasabah.getNama()+", saldo tidak mencukupi");}
    }
    
    private void setJmlUang(double jumlahUang)throws Exception{
        try{
            if(!noRekening.isEmpty()){this.jmlUang = jumlahUang;}
        }
        catch(Exception e){throw new Exception ("Masukan No Rekening terlebih dahulu");}
    }
    public double getJmlUang(){
        return jmlUang;
    }
    private void setNorekening(Nasabah nasabah){
        this.noRekening= nasabah.getNoRekening();
    }
}


/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package nasabah_bank;

import java.util.logging.Level;
import java.util.logging.Logger;

/**
 *
 * @author Asus X452E
 */
public class Nasabah_Bank {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        KTP ktp1=new KTP();
        KTP ktp2=new KTP();
        Nasabah nasabah1=new Nasabah();
        Nasabah nasabah2=new Nasabah();
        Transaksi simpan1=new Transaksi();
        Transaksi simpan2=new Transaksi();
        
        ktp2.setNama("B");
        ktp2.setAlamat("bonsay", "jakarta", "DKI", "jaktim", "jatinegara");
        ktp2.setJk("lk");
        ktp2.setAgama("islam");
        
        ktp1.setNama("A");
        ktp1.setAlamat("bonasel", "jakarta", "DKI", "jaktim", "jatinegara");
        ktp1.setJk("lk");
        ktp1.setAgama("Hindu");
        
        try {
            nasabah2.setNasabah(ktp2,"747475",20000,"43534", "Mandiri", "jakarta");
        } catch (Exception ex) {
            System.out.println("terjadi error "+ex.getMessage());
        }
        
        try {
            nasabah1.setNasabah(ktp1,"34634",10000,"43534", "BRI", "jakarta");
        } catch (Exception ex) {
            System.out.println("terjadi error "+ex.getMessage());
        }
        
        try {
            simpan2.simpanUang(nasabah2, 50000);
        } catch (Exception ex) {
            System.out.println("terjadi error "+ex.getMessage());
        }
        
        try {
            simpan2.kirimUang(nasabah2, nasabah1, 20000);
        } catch (Exception ex) {
            System.out.println("terjadi error "+ex.getMessage());
        }
        
        
        //nasabah 1
        System.out.println("Nama   : "+nasabah1.getNama());
        System.out.println("Alamat : "+nasabah1.getAlamat());
        try {
            System.out.println("Bank "+nasabah1.getBank());
        } catch (Exception ex) {
            System.out.println("terjadi error "+ex.getMessage());
        }
        System.out.println("jumlah uang "+nasabah1.getJmlUang());
        
        
        //nasabah 2
        System.out.println("Nama   : "+nasabah2.getNama());
        System.out.println("Alamat : "+nasabah2.getAlamat());
        try {
            System.out.println("Bank "+nasabah2.getBank());
        } catch (Exception ex) {
            System.out.println("terjadi error "+ex.getMessage());
        }
        System.out.println("jumlah uang "+nasabah2.getJmlUang());
       
        
    
}

}

