<h2 align="center">🖥️ Hyper-V Virtualization-Based System and Network Management Lab</h2>



<p align="center">

&#x20; <img src="https://img.shields.io/badge/Platform-Hyper--V-0078D4?style=for-the-badge\&logo=windows\&logoColor=white"/>

&#x20; <img src="https://img.shields.io/badge/OS-Windows%2011-0078D4?style=for-the-badge\&logo=windows11\&logoColor=white"/>

&#x20; <img src="https://img.shields.io/badge/Type-Virtualization%20Lab-green?style=for-the-badge"/>

</p>



<p>

<b>TR:</b> Bu projemde Hyper-V sanallaştırma platformunu kullanarak Windows 11 sanal makinesi kurdum. Kurulum sürecinde sanal makine oluşturma, disk işlemleri, checkpoint yapısı, export/import işlemleri ve network tipleri gibi birçok konuda uygulamalı çalışma yapma fırsatı buldum.
</p>

<p>

<b>EN:</b> In this project, I created a Windows 11 virtual machine using the Hyper-V virtualization platform. During the setup process, I had the opportunity to work practically on many topics such as virtual machine creation, disk management, checkpoints, export/import operations, and different network types. At the same time, this project allowed me to apply the knowledge I learned about converter tools in practice.

</p>



\---



\## 📋 Table of Contents



\- \[Virtual Machine Settings](#%EF%B8%8F-virtual-machine-settings--sanal-makine-ayarları)

\- \[Disk Adding And Expanding](#-disk-adding-and-expanding--disk-ekleme-ve-genişletme)

\- \[Checkpoints](#-checkpoints)

\- \[Export And Import](#-virtual-machine-export-and-import--dışa-ve-içeri-aktarma)

\- \[Virtualization Networks](#-virtualization-networks--sanallaştırma-networkleri)



\---



<h2>⚙️ Virtual Machine Settings / Sanal Makine Ayarları</h2>



<table>

&#x20; <tr>

&#x20;   <td align="center" width="33%">

&#x20;     <img src="screenshots/1-virtual_switch_manager.png" width="100%" alt="Virtual Switch Manager"/>

&#x20;     <br/><sub><b>1 — Virtual Switch Manager</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="33%">

&#x20;     <img src="screenshots/2-virtual_machine_settings.png" width="100%" alt="VM Settings"/>

&#x20;     <br/><sub><b>2 — VM General Settings</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="33%">

&#x20;     <img src="screenshots/3-virtual_machine_disk.png" width="100%" alt="VM Disk"/>

&#x20;     <br/><sub><b>3 — VM Disk Configuration</b></sub>

&#x20;   </td>

&#x20; </tr>

</table>



<table>

&#x20; <tr>

&#x20;   <td>

&#x20;     <p>

&#x20;       <b>TR:</b> İlk görselde Hyper-V platformunda network ayarlarımı ve isimlendirmeleri yaptım. Burada yaptığım ayarlara göre kuracağım sanal makinelerde belirlediğim network yapılarını kullanacağım. Bu sayede sanal makineler arasında daha düzenli ve kontrollü bir ağ yapısı oluşturmuş oldum.

&#x20;     </p>

&#x20;     <p>

&#x20;       İkinci görselde ise sanal makinemin genel ayarları bulunuyor. İşletim sistemini ISO dosyası ile kuracağım için boot order kısmında ISO'yu en üste aldım. Sanal makineye başlangıç olarak 4 GB RAM, 100 GB disk alanı ve 6 sanal işlemci tanımladım. Network tarafında daha önce oluşturduğum bridged network yapısını kullandım. Ayrıca Integration Services kısmında sistemi daha stabil ve performanslı kullanabilmek için gerekli ayarları aktif hale getirdim.

&#x20;     </p>

&#x20;     <p>

&#x20;       Üçüncü görselde ise işletim sistemi kurulumu sırasında kullandığım diskin boyutunu ve isimlendirmesini görebilirsiniz.

&#x20;     </p>

&#x20;     <br/>

&#x20;     <p>

&#x20;       <b>EN:</b> In the first screenshot, I configured the network settings and naming structure on the Hyper-V platform. Based on these settings, I will use the defined network configurations for the virtual machines. This helped me create a more organized and controlled network structure between virtual machines.

&#x20;     </p>

&#x20;     <p>

&#x20;       In the second screenshot, you can see the general settings of my virtual machine. Since I will install the OS using an ISO file, I moved it to the top of the boot order. I assigned 4 GB of RAM, 100 GB of disk space, and 6 virtual processors. I also used the bridged network I created earlier and enabled Integration Services for better stability and performance.

&#x20;     </p>

&#x20;     <p>

&#x20;       In the third screenshot, you can see the disk size and naming configuration used during the OS installation.

&#x20;     </p>

&#x20;   </td>

&#x20; </tr>

</table>



\---



<h2>💾 Disk Adding And Expanding / Disk Ekleme Ve Genişletme</h2>



<table>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/4-disk_befor.png" width="100%" alt="Disk Before"/>

&#x20;     <br/><sub><b>Before / Önce</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/4-disk_after.png" width="100%" alt="Disk After"/>

&#x20;     <br/><sub><b>After / Sonra</b></sub>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td colspan="2">

&#x20;     <p>

&#x20;       <b>TR:</b> Projede sanal makine üzerinde disk genişletme ve yeni disk ekleme işlemleri gerçekleştirdim. İlk görselde diskin işlem yapılmadan önceki hali yer almaktadır. İkinci görselde ise mevcut diski 30 GB genişlettim; bunun sebebi disk alanının yetersiz kalması ve aynı disk üzerinde çalışmaya devam edecek olmamdı. Daha sonra sisteme 50 GB boyutunda yeni bir disk ekleyerek ana sistem diskinde oluşabilecek doluluk sorunlarının önüne geçmeyi hedefledim.

&#x20;     </p>

&#x20;     <p>

&#x20;       <b>EN:</b> In this project, I performed disk extension and new disk addition operations on the virtual machine. The first image shows the disk before any modifications. In the second image, I extended the existing disk by 30 GB due to insufficient storage space. After that, I added a new 50 GB disk to the system to prevent the main disk from running out of space.

&#x20;     </p>

&#x20;   </td>

&#x20; </tr>

</table>



\---



<h2>📸 Checkpoints</h2>



<table>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/6-checkpoint1.png" width="100%" alt="Checkpoint 1"/>

&#x20;     <br/><sub><b>1 — Stable State / Kararlı Durum</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/7-checkpoint2.png" width="100%" alt="Checkpoint 2"/>

&#x20;     <br/><sub><b>2 — Black Screen Error / Siyah Ekran Hatası</b></sub>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/8-checkpoint3.png" width="100%" alt="Checkpoint 3"/>

&#x20;     <br/><sub><b>3 — Checkpoint Manager</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/9-checkpoint4.png" width="100%" alt="Checkpoint 4"/>

&#x20;     <br/><sub><b>4 — Restored State / Geri Yükleme</b></sub>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td colspan="2">

&#x20;     <p>

&#x20;       <b>TR:</b> Bu projede, sistem üzerinde yapılacak riskli işlemler öncesinde checkpoint kullanımını test ettim. İlk görselde stabil çalışan sistemin checkpoint'ini aldım. Daha sonra şüpheli bir işlem gerçekleştirdim ve ikinci görselde görüldüğü gibi siyah ekran hatası oluştu. Bu hata sonrasında Hyper-V checkpoint arayüzü üzerinden önceki checkpoint'e dönerek sistemi hızla eski haline getirdim.

&#x20;     </p>

&#x20;     <p>

&#x20;       Ayrıca bu projede <b>Standard</b> ve <b>Production Checkpoint</b> arasındaki farkları da inceleme fırsatı buldum. Production Checkpoint, VSS (Volume Shadow Copy Service) desteği sayesinde uygulamalara verilerini diske kaydetmeleri için bildirim göndererek daha tutarlı bir yedekleme yapısı oluşturur. Standard Checkpoint ise sanal makineyi RAM dahil checkpoint anındaki tam haliyle geri yükler.

&#x20;     </p>

&#x20;     <br/>

&#x20;     <p>

&#x20;       <b>EN:</b> In this project, I tested checkpoint usage before performing risky operations. In the first screenshot, I created a checkpoint while the system was running stably. After performing a suspicious operation, a black screen error occurred as shown in the second screenshot. I then reverted to the previous checkpoint through the Hyper-V interface to quickly restore the system.

&#x20;     </p>

&#x20;     <p>

&#x20;       I also examined the differences between <b>Standard</b> and <b>Production Checkpoint</b>. Production Checkpoint uses VSS (Volume Shadow Copy Service) to notify supported applications to flush data to disk before the checkpoint is taken, ensuring a more consistent backup. Standard Checkpoint restores the VM exactly as it was at the moment it was taken, including RAM data.

&#x20;     </p>

&#x20;   </td>

&#x20; </tr>

</table>



\---



<h2>📦 Virtual Machine Export And Import / Dışa ve İçeri Aktarma</h2>



<table>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/10-export1.png" width="100%" alt="Export Step 1"/>

&#x20;     <br/><sub><b>Export — Step 1 / Adım 1</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/11-export2.png" width="100%" alt="Export Step 2"/>

&#x20;     <br/><sub><b>Export — Step 2 / Adım 2</b></sub>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/12-import1.png" width="100%" alt="Import Step 1"/>

&#x20;     <br/><sub><b>Import — Step 1 / Adım 1</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/13-import2.png" width="100%" alt="Import Step 2"/>

&#x20;     <br/><sub><b>Import — Step 2 / Adım 2</b></sub>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td colspan="2">

&#x20;     <p>

&#x20;       <b>TR:</b> Bu aşamada ilk iki görselde export, son iki görselde ise import işlemlerini gerçekleştirdim. Export işleminin amacı, oluşturduğum sanal makineyi farklı platformlara veya ortamlara kolayca taşıyabilmektir. Import işlemi ise export edilen sanal makinenin farklı bir ortama yeniden kurulmasını sağlar. Bu yöntem sistem taşınabilirliği ve hızlı kurulum açısından büyük avantaj sunar.

&#x20;     </p>

&#x20;     <p>

&#x20;       <b>EN:</b> At this stage, I performed export operations in the first two images and import operations in the last two. The export process allows the virtual machine to be easily transferred to different platforms or environments. The import process enables the exported VM to be deployed in a new environment, providing significant advantages in terms of portability and rapid deployment.

&#x20;     </p>

&#x20;   </td>

&#x20; </tr>

</table>



\---



<h2>🌐 Virtualization Networks / Sanallaştırma Networkleri</h2>



<table>

&#x20; <tr>

&#x20;   <td colspan="2">

&#x20;     <p>

&#x20;       <b>TR:</b> Sanallaştırma networkleri, sanal makinelerin (VM), host sistemlerin ve LAN yapılarının birbirleriyle iletişim kurmasını sağlar. Hyper-V'de üç temel network tipi kullanılmaktadır:

&#x20;     </p>

&#x20;     <ul>

&#x20;       <li><b>External (Bridged):</b> VM'ler; birbirleriyle, fiziksel host ile ve hostun bağlı olduğu LAN ağıyla iletişim kurabilir. VMware'deki Bridge yapısına karşılık gelir.</li>

&#x20;       <li><b>Internal (Host-Only):</b> VM'ler yalnızca birbirleriyle ve fiziksel host ile haberleşebilir. LAN'daki diğer cihazlara erişim yoktur.</li>

&#x20;       <li><b>Private (Internal):</b> Yalnızca sanal makineler arasında iletişim kurulabilir. Host veya dış ağ ile bağlantı bulunmaz. Tamamen izole lab ortamları için idealdir.</li>

&#x20;     </ul>

&#x20;     <br/>

&#x20;     <p>

&#x20;       <b>EN:</b> Virtualization networks enable communication between VMs, host systems, and LAN structures. Hyper-V uses three main network types:

&#x20;     </p>

&#x20;     <ul>

&#x20;       <li><b>External (Bridged):</b> VMs can communicate with each other, the physical host, and the host's LAN network. Equivalent to VMware's Bridge mode.</li>

&#x20;       <li><b>Internal (Host-Only):</b> VMs can only communicate with each other and the physical host. No access to other LAN devices.</li>

&#x20;       <li><b>Private (Internal):</b> Communication only between VMs. No connection to the host or external networks. Ideal for fully isolated lab environments.</li>

&#x20;     </ul>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/14-virtual_switch_manager.png" width="100%" alt="Virtual Switch Manager"/>

&#x20;     <br/><sub><b>1 — Virtual Switch Manager / Network Yapıları</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/15-virtual_machine_bridged.png" width="100%" alt="Bridged Network"/>

&#x20;     <br/><sub><b>2 — Bridged Network Integration</b></sub>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/16-virtual_machine_bridged2.png" width="100%" alt="Ping Test"/>

&#x20;     <br/><sub><b>3 — Ping Test / Bağlantı Doğrulama</b></sub>

&#x20;   </td>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/17-virtual_machine_hostonly.png" width="100%" alt="Host-Only Network"/>

&#x20;     <br/><sub><b>4 — Host-Only Network</b></sub>

&#x20;   </td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td align="center" width="50%">

&#x20;     <img src="screenshots/18-virtual_machine_internal.png" width="100%" alt="Internal Network"/>

&#x20;     <br/><sub><b>5 — Internal Network</b></sub>

&#x20;   </td>

&#x20;   <td></td>

&#x20; </tr>

&#x20; <tr>

&#x20;   <td colspan="2">

&#x20;     <p>

&#x20;       <b>TR:</b> İlk görselde farklı senaryolar için oluşturduğum network yapılarını görebilirsiniz. İkinci görselde Windows 11 sanal makineme "bridged" network yapısını entegre ettim; bu sayede sanal makine fiziksel makinemle, diğer VM'lerle ve LAN ağıyla iletişim kurabilir hale geldi. Üçüncü görselde fiziksel makineme ping testi yaparak bağlantıyı doğruladım.

&#x20;     </p>

&#x20;     <p>

&#x20;       Host-Only yapısında statik IP tanımlaması gerekir: fiziksel makinede oluşan sanal adaptörün network ID'si ile aynı subnet yapısında bir IP adresi sanal makineye manuel olarak atanır. Internal yapısında ise aynı network ID'yi kullanan VM'ler birbirleriyle haberleşebilir; her VM'nin farklı bir IP adresine sahip olması gerekmektedir.

&#x20;     </p>

&#x20;     <br/>

&#x20;     <p>

&#x20;       <b>EN:</b> In the first screenshot, you can see the network configurations I created for different scenarios. In the second screenshot, I integrated the "bridged" network into my Windows 11 VM, allowing it to communicate with the physical machine, other VMs, and the LAN. I verified the connection with a ping test in the third screenshot.

&#x20;     </p>

&#x20;     <p>

&#x20;       For Host-Only, a static IP must be manually assigned using the same subnet as the virtual adapter on the physical machine. For the Internal network, VMs sharing the same network ID can communicate with each other, as long as each VM has a unique IP address.

&#x20;     </p>

&#x20;   </td>

&#x20; </tr>

</table>

