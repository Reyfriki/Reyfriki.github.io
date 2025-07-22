<html lang="es">
 <head>
  <meta charset="utf-8" />
  <meta content="width=device-width, initial-scale=1" name="viewport" />
  <title>ReyFriki Juegos - Subir Mods</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link
   href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"
   rel="stylesheet"
  />
  <style>
   @import url("https://fonts.googleapis.com/css2?family=Comic+Neue:wght@700&display=swap");
   .font-comic {
    font-family: "Comic Neue", cursive;
   }
   /* Scrollbar styling for the scrollable list */
   .scrollbar-thin::-webkit-scrollbar {
    width: 6px;
   }
   .scrollbar-thin::-webkit-scrollbar-track {
    background: transparent;
   }
   .scrollbar-thin::-webkit-scrollbar-thumb {
    background-color: #991b1b;
    /* Tailwind red-800 */
    border-radius: 10px;
   }
   /* Hover and selected styles for list items */
   .nav-list li,
   #gameList li,
   #emuladoresList li,
   #extraList li,
   #bioContent,
   #modsList li {
    transition: color 0.2s ease;
    cursor: pointer;
    padding: 0.25rem 0;
   }
   .nav-list li:hover,
   #gameList li:hover,
   #emuladoresList li:hover,
   #extraList li:hover,
   #modsList li:hover {
    color: #dc2626;
    /* Tailwind red-600 */
   }
   .nav-list li.selected {
    color: #b91c1c;
    /* Tailwind red-700 */
    font-weight: 700;
   }
   #gameList li.selected,
   #emuladoresList li.selected,
   #extraList li.selected,
   #modsList li.selected {
    color: #b91c1c;
    /* Tailwind red-700 */
    font-weight: 700;
   }
   /* Background with Spiderman comic style */
   body {
    background-image: url("https://wallpaperaccess.com/full/317501.jpg");
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
   }
   /* Overlay to darken background */
   #overlay {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, 0.75);
    z-index: -1;
   }
  </style>
 </head>
 <body class="relative min-h-screen flex flex-col items-start justify-start font-comic text-white">
  <div id="overlay"></div>
  <header class="w-full max-w-7xl flex items-center justify-start px-4 py-3">
   <h1
    class="text-4xl text-red-600 select-none"
    style="text-shadow: 0 0 4px #b91c1c, 0 0 8px #b91c1c, 0 0 12px #b91c1c"
   >
    ReyFriki
   </h1>
  </header>
  <main
   class="flex flex-col md:flex-row items-start justify-start gap-6 mt-6 w-full max-w-7xl px-4 pb-20"
  >
   <nav
    class="bg-black bg-opacity-70 rounded-md shadow-lg w-40 text-left font-semibold text-sm select-none"
   >
    <ul class="nav-list py-2 px-4 text-white">
     <li
      data-section="emuladores"
      class="py-2 rounded-t-md hover:bg-red-700 cursor-pointer"
      >Emuladores</li
     >
     <li data-section="juegos" class="py-2 hover:bg-red-700 cursor-pointer"
      >Juegos</li
     >
     <li data-section="extra" class="py-2 hover:bg-red-700 cursor-pointer"
      >Extra</li
     >
     <li
      data-section="reyfriki"
      class="py-2 hover:bg-red-700 cursor-pointer"
      >ReyFriki</li
     >
     <li
      data-section="mods"
      class="py-2 rounded-b-md hover:bg-red-700 cursor-pointer"
      >Mods Subidos</li
     >
     <li
      data-section="upload"
      class="py-2 rounded-b-md hover:bg-red-700 cursor-pointer"
      >Subir Mods</li
     >
    </ul>
   </nav>
   <section
    class="flex flex-col gap-3 w-full max-w-4xl bg-black bg-opacity-70 rounded-md shadow-lg p-6 text-white text-base min-h-[24rem] overflow-y-auto scrollbar-thin pr-4"
   >
    <!-- Emuladores list -->
    <ul
     id="emuladoresList"
     class="max-h-[28rem] font-semibold space-y-2 cursor-pointer hidden"
    >
     <li data-game="Emulador 1">Emulador 1</li>
     <li data-game="Emulador 2">Emulador 2</li>
     <li data-game="Emulador 3">Emulador 3</li>
     <li data-game="Emulador 4">Emulador 4</li>
     <li data-game="Emulador 5">Emulador 5</li>
    </ul>
    <!-- Juegos list -->
    <ul
     id="gameList"
     class="max-h-[28rem] font-semibold space-y-2 cursor-pointer hidden"
    >
     <li data-game="Operation Raccoon City">Operation Raccoon City</li>
    </ul>
    <!-- Extra list -->
    <ul
     id="extraList"
     class="max-h-[28rem] font-semibold space-y-2 cursor-pointer hidden"
    >
     <li data-game="Extra 1">Extra 1</li>
     <li data-game="Extra 2">Extra 2</li>
     <li data-game="Extra 3">Extra 3</li>
     <li data-game="Extra 4">Extra 4</li>
     <li data-game="Extra 5">Extra 5</li>
    </ul>
    <!-- ReyFriki bio content -->
    <article
     id="bioContent"
     class="hidden text-gray-300 leading-relaxed select-text"
    >
     <h2 class="text-2xl font-bold mb-4 text-red-600">ReyFriki</h2>
     <p>
      ReyFriki es un apasionado de la tecnología y los videojuegos, dedicado a
      optimizar y compartir contenido para la mejor experiencia de juego. Su
      misión es ofrecer recursos y guías para que los usuarios disfruten al
      máximo sus juegos favoritos y herramientas tecnológicas.
     </p>
     <p class="mt-4">
      Con años de experiencia en la comunidad gamer y tecnológica, ReyFriki se
      ha convertido en un referente para quienes buscan calidad y optimización
      en sus proyectos digitales.
     </p>
    </article>
    <!-- Mods uploaded list -->
    <ul
     id="modsList"
     class="max-h-[28rem] font-semibold space-y-2 cursor-pointer hidden"
    >
     <!-- Dynamically added mods will appear here -->
    </ul>
    <!-- Mods upload section -->
    <section id="modsSection" class="hidden">
     <h2 class="text-2xl font-bold mb-4 text-red-600">Subir Mods</h2>
     <form
      id="modUploadForm"
      class="flex flex-col gap-4"
      enctype="multipart/form-data"
      novalidate
     >
      <label class="flex flex-col text-white font-semibold">
       Nombre del Mod:
       <input
        type="text"
        name="modName"
        required
        class="mt-1 rounded-md bg-gray-800 text-white px-3 py-2 focus:outline-none focus:ring-2 focus:ring-red-600"
        placeholder="Nombre del mod"
       />
      </label>
      <label class="flex flex-col text-white font-semibold">
       Descripción:
       <textarea
        name="modDescription"
        rows="4"
        required
        class="mt-1 rounded-md bg-gray-800 text-white px-3 py-2 resize-none focus:outline-none focus:ring-2 focus:ring-red-600"
        placeholder="Descripción del mod"
       ></textarea>
      </label>
      <label class="flex flex-col text-white font-semibold">
       Archivo del Mod:
       <input
        type="file"
        name="modFile"
        accept=".zip,.rar,.7z,.mod,.exe"
        required
        class="mt-1 text-white"
       />
      </label>
      <button
       type="submit"
       class="bg-red-700 hover:bg-red-800 rounded-md px-4 py-2 font-semibold transition-colors duration-200"
      >
       Subir Mod
      </button>
      <p id="uploadMessage" class="text-sm mt-2"></p>
     </form>
    </section>
   </section>
  </main>
  <footer
   id="downloadBar"
   class="fixed bottom-4 left-4 w-full max-w-4xl bg-black bg-opacity-80 rounded-md shadow-lg p-4 flex items-center justify-between gap-6 text-white text-base font-semibold select-none opacity-0 pointer-events-none transition-opacity duration-300"
  >
   <div class="flex items-center gap-3">
    <i class="fas fa-arrow-down text-lg"></i>
    <span id="downloadGameName">Descargas</span>
   </div>
   <div class="flex gap-4">
    <a
     id="downloadLink"
     href="#"
     target="_blank"
     rel="noopener noreferrer"
     class="bg-gray-900 hover:bg-gray-800 rounded px-4 py-2 text-lg inline-block"
     >GoFile</a
    >
   </div>
  </footer>
  <script>
   const navList = document.querySelectorAll(".nav-list li[data-section]");
   const emuladoresList = document.getElementById("emuladoresList");
   const gameList = document.getElementById("gameList");
   const extraList = document.getElementById("extraList");
   const bioContent = document.getElementById("bioContent");
   const modsSection = document.getElementById("modsSection");
   const modsList = document.getElementById("modsList");
   const downloadBar = document.getElementById("downloadBar");
   const downloadGameName = document.getElementById("downloadGameName");
   const downloadLink = document.getElementById("downloadLink");
   const modUploadForm = document.getElementById("modUploadForm");
   const uploadMessage = document.getElementById("uploadMessage");

   // Store uploaded mods in localStorage
   let uploadedMods = JSON.parse(localStorage.getItem("uploadedMods") || "[]");

   // Function to hide all content sections
   function hideAllSections() {
    emuladoresList.classList.add("hidden");
    gameList.classList.add("hidden");
    extraList.classList.add("hidden");
    bioContent.classList.add("hidden");
    modsSection.classList.add("hidden");
    modsList.classList.add("hidden");
    // Remove selected from all nav items
    navList.forEach((li) => li.classList.remove("selected"));
    // Remove selected from all list items
    [emuladoresList, gameList, extraList, modsList].forEach((list) => {
     list.querySelectorAll("li").forEach((li) => li.classList.remove("selected"));
    });
    // Hide download bar
    downloadBar.style.opacity = "0";
    downloadBar.style.pointerEvents = "none";
    uploadMessage.textContent = "";
    modUploadForm.reset();
    downloadLink.href = "#";
   }

   // Show default section Juegos on load
   window.addEventListener("DOMContentLoaded", () => {
    renderModsList();
    hideAllSections();
    gameList.classList.remove("hidden");
    navList.forEach((li) => {
     if (li.dataset.section === "juegos") li.classList.add("selected");
    });
   });

   // Nav click handler
   navList.forEach((li) => {
    li.addEventListener("click", () => {
     hideAllSections();
     const section = li.dataset.section;
     if (section === "emuladores") {
      emuladoresList.classList.remove("hidden");
     } else if (section === "juegos") {
      gameList.classList.remove("hidden");
     } else if (section === "extra") {
      extraList.classList.remove("hidden");
     } else if (section === "reyfriki") {
      bioContent.classList.remove("hidden");
     } else if (section === "mods") {
      modsList.classList.remove("hidden");
     } else if (section === "upload") {
      modsSection.classList.remove("hidden");
     }
     li.classList.add("selected");
    });
   });

   // Function to render mods list
   function renderModsList() {
    modsList.innerHTML = "";
    uploadedMods.forEach((mod, index) => {
     const li = document.createElement("li");
     li.classList.add(
      "cursor-pointer",
      "transition-colors",
      "duration-200",
      "hover:text-red-600",
      "font-semibold",
      "flex",
      "justify-between",
      "items-center",
      "gap-2"
     );
     li.dataset.index = index;

     const spanName = document.createElement("span");
     spanName.textContent = mod.name;
     li.appendChild(spanName);

     const downloadBtn = document.createElement("a");
     downloadBtn.href = mod.url;
     downloadBtn.target = "_blank";
     downloadBtn.rel = "noopener noreferrer";
     downloadBtn.textContent = "Descargar";
     downloadBtn.className =
      "bg-gray-900 hover:bg-gray-800 rounded px-3 py-1 text-sm inline-block";
     li.appendChild(downloadBtn);

     modsList.appendChild(li);
    });
   }

   // Mods list click handler to highlight selected mod and show download bar
   modsList.addEventListener("click", (e) => {
    const li = e.target.closest("li[data-index]");
    if (!li) return;
    modsList.querySelectorAll("li").forEach((item) =>
     item.classList.remove("selected")
    );
    li.classList.add("selected");
    const modIndex = li.dataset.index;
    if (modIndex !== undefined && uploadedMods[modIndex]) {
     const mod = uploadedMods[modIndex];
     downloadGameName.textContent = `Descargas - ${mod.name}`;
     downloadLink.href = mod.url;
     downloadBar.style.opacity = "1";
     downloadBar.style.pointerEvents = "auto";
     window.scrollTo({ top: document.body.scrollHeight, behavior: "smooth" });
    }
   });

   // Game/emulador/extra item click handler
   [emuladoresList, gameList, extraList].forEach((list) => {
    list.addEventListener("click", (e) => {
     const li = e.target.closest("li[data-game]");
     if (!li) return;
     // Remove selected class from all in this list
     list.querySelectorAll("li").forEach((item) =>
      item.classList.remove("selected")
     );
     // Add selected class to clicked
     li.classList.add("selected");
     const gameName = li.getAttribute("data-game");
     downloadGameName.textContent = `Descargas - ${gameName}`;
     // Show the download bar
     downloadBar.style.opacity = "1";
     downloadBar.style.pointerEvents = "auto";
     // Reset download link for non-mods
     downloadLink.href = "#";
     // Scroll to bottom so user sees the bar on mobile
     window.scrollTo({ top: document.body.scrollHeight, behavior: "smooth" });
    });
   });

   // Handle mod upload form submission
   modUploadForm.addEventListener("submit", (e) => {
    e.preventDefault();
    uploadMessage.textContent = "";
    const formData = new FormData(modUploadForm);
    const modName = formData.get("modName").trim();
    const modDescription = formData.get("modDescription").trim();
    const modFile = formData.get("modFile");

    if (!modName || !modDescription || !modFile.name) {
     uploadMessage.textContent =
      "Por favor, completa todos los campos y selecciona un archivo.";
     uploadMessage.classList.remove("text-green-500");
     uploadMessage.classList.add("text-red-500");
     return;
    }

    // Simulate upload process (since no backend)
    uploadMessage.textContent = "Subiendo mod...";
    uploadMessage.classList.remove("text-red-500");
    uploadMessage.classList.add("text-yellow-400");

    // Create a local URL for the uploaded file to simulate download link
    const fileURL = URL.createObjectURL(modFile);

    setTimeout(() => {
     uploadMessage.textContent = "Mod subido con éxito. ¡Gracias por contribuir!";
     uploadMessage.classList.remove("text-yellow-400");
     uploadMessage.classList.add("text-green-500");

     // Add mod to uploadedMods array and save to localStorage
     uploadedMods.push({
      name: modName,
      description: modDescription,
      url: fileURL,
     });
     localStorage.setItem("uploadedMods", JSON.stringify(uploadedMods));

     // Render mods list and switch to Mods Subidos section
     renderModsList();
     hideAllSections();
     modsList.classList.remove("hidden");
     navList.forEach((liNav) => {
      if (liNav.dataset.section === "mods") liNav.classList.add("selected");
     });

     // Select the newly added mod
     modsList.querySelectorAll("li").forEach((item) =>
      item.classList.remove("selected")
     );
     const newModLi = Array.from(modsList.children).find(
      (li) => li.dataset.index == uploadedMods.length - 1
     );
     if (newModLi) {
      newModLi.classList.add("selected");
      downloadGameName.textContent = `Descargas - ${modName}`;
      downloadLink.href = fileURL;
      downloadBar.style.opacity = "1";
      downloadBar.style.pointerEvents = "auto";
     }

     modUploadForm.reset();
    }, 2000);
   });
  </script>
 </body>
</html>
