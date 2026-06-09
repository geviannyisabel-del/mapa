[mapa_conceptual_ia.html](https://github.com/user-attachments/files/28738433/mapa_conceptual_ia.html)

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:var(--font-sans)}
.map-container{padding:1.5rem 1rem;min-height:600px;position:relative}
.map-title{text-align:center;font-size:22px;font-weight:500;color:var(--color-text-primary);margin-bottom:0.4rem}
.map-subtitle{text-align:center;font-size:13px;color:var(--color-text-secondary);margin-bottom:1.5rem}
svg#mindmap{width:100%;display:block}
.node{cursor:pointer;transition:all 0.2s}
.node rect,.node ellipse{transition:all 0.2s}
.node:hover rect,.node:hover ellipse{filter:brightness(0.93)}
.panel{background:var(--color-background-primary);border:0.5px solid var(--color-border-secondary);border-radius:var(--border-radius-lg);padding:1.25rem;margin-top:1.2rem;animation:fadeIn 0.25s ease}
@keyframes fadeIn{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}
.panel-title{font-size:16px;font-weight:500;color:var(--color-text-primary);margin-bottom:0.5rem;display:flex;align-items:center;gap:8px}
.panel-desc{font-size:14px;color:var(--color-text-secondary);line-height:1.6;margin-bottom:1rem}
.links-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:8px}
.link-card{background:var(--color-background-secondary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-md);padding:0.6rem 0.8rem;text-decoration:none;display:flex;align-items:center;gap:8px;transition:border-color 0.15s}
.link-card:hover{border-color:var(--color-border-primary)}
.link-card span{font-size:13px;color:var(--color-text-primary);font-weight:400}
.link-card i{font-size:16px;flex-shrink:0}
.badge{display:inline-block;font-size:11px;padding:2px 8px;border-radius:var(--border-radius-md);font-weight:500;margin-left:8px}
.close-btn{margin-left:auto;background:none;border:none;cursor:pointer;color:var(--color-text-secondary);font-size:18px;line-height:1}
.hint{text-align:center;font-size:12px;color:var(--color-text-tertiary);margin-top:0.5rem}
</style>

<div class="map-container">
  <h2 class="map-title">Inteligencia Artificial</h2>
  <p class="map-subtitle">Haz clic en cualquier nodo para explorar el tema</p>

  <svg id="mindmap" viewBox="0 0 700 500" xmlns="http://www.w3.org/2000/svg">
    <defs>
      <marker id="arr" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto">
        <path d="M0,0 L0,6 L8,3 z" fill="#888780"/>
      </marker>
    </defs>

    <!-- Connector lines -->
    <!-- Center to ML -->
    <line x1="350" y1="210" x2="180" y2="150" stroke="#888780" stroke-width="1.2" stroke-dasharray="4,3" marker-end="url(#arr)"/>
    <!-- Center to DL -->
    <line x1="350" y1="210" x2="520" y2="150" stroke="#888780" stroke-width="1.2" stroke-dasharray="4,3" marker-end="url(#arr)"/>
    <!-- Center to NLP -->
    <line x1="350" y1="250" x2="170" y2="320" stroke="#888780" stroke-width="1.2" stroke-dasharray="4,3" marker-end="url(#arr)"/>
    <!-- Center to Vision -->
    <line x1="350" y1="250" x2="530" y2="320" stroke="#888780" stroke-width="1.2" stroke-dasharray="4,3" marker-end="url(#arr)"/>
    <!-- Center to Ética -->
    <line x1="350" y1="270" x2="350" y2="380" stroke="#888780" stroke-width="1.2" stroke-dasharray="4,3" marker-end="url(#arr)"/>
    <!-- ML to DL subtle -->
    <line x1="230" y1="140" x2="430" y2="140" stroke="#B4B2A9" stroke-width="0.8" stroke-dasharray="3,4"/>

    <!-- CENTER NODE: IA -->
    <g class="node" id="n-ia" onclick="showPanel('ia')">
      <ellipse cx="350" cy="240" rx="68" ry="38" fill="#534AB7" rx="12"/>
      <text x="350" y="235" text-anchor="middle" font-size="15" font-weight="500" fill="#EEEDFE">Inteligencia</text>
      <text x="350" y="252" text-anchor="middle" font-size="15" font-weight="500" fill="#EEEDFE">Artificial</text>
    </g>

    <!-- ML -->
    <g class="node" id="n-ml" onclick="showPanel('ml')">
      <rect x="100" y="108" width="160" height="52" rx="8" fill="#1D9E75"/>
      <text x="180" y="130" text-anchor="middle" font-size="13" font-weight="500" fill="#E1F5EE">Machine</text>
      <text x="180" y="148" text-anchor="middle" font-size="13" font-weight="500" fill="#E1F5EE">Learning</text>
    </g>

    <!-- DL -->
    <g class="node" id="n-dl" onclick="showPanel('dl')">
      <rect x="440" y="108" width="160" height="52" rx="8" fill="#185FA5"/>
      <text x="520" y="130" text-anchor="middle" font-size="13" font-weight="500" fill="#E6F1FB">Deep</text>
      <text x="520" y="148" text-anchor="middle" font-size="13" font-weight="500" fill="#E6F1FB">Learning</text>
    </g>

    <!-- NLP -->
    <g class="node" id="n-nlp" onclick="showPanel('nlp')">
      <rect x="80" y="295" width="175" height="52" rx="8" fill="#993C1D"/>
      <text x="167" y="317" text-anchor="middle" font-size="13" font-weight="500" fill="#FAECE7">Procesamiento</text>
      <text x="167" y="335" text-anchor="middle" font-size="13" font-weight="500" fill="#FAECE7">del Lenguaje (NLP)</text>
    </g>

    <!-- Vision Computacional -->
    <g class="node" id="n-cv" onclick="showPanel('cv')">
      <rect x="445" y="295" width="175" height="52" rx="8" fill="#993556"/>
      <text x="532" y="317" text-anchor="middle" font-size="13" font-weight="500" fill="#FBEAF0">Visión</text>
      <text x="532" y="335" text-anchor="middle" font-size="13" font-weight="500" fill="#FBEAF0">Computacional</text>
    </g>

    <!-- Ética -->
    <g class="node" id="n-etica" onclick="showPanel('etica')">
      <rect x="270" y="388" width="160" height="48" rx="8" fill="#BA7517"/>
      <text x="350" y="408" text-anchor="middle" font-size="13" font-weight="500" fill="#FAEEDA">Ética e</text>
      <text x="350" y="426" text-anchor="middle" font-size="13" font-weight="500" fill="#FAEEDA">Impacto Social</text>
    </g>

    <!-- Sub-nodes ML -->
    <g class="node" onclick="showPanel('supervisado')">
      <rect x="40" y="52" width="110" height="36" rx="6" fill="#9FE1CB"/>
      <text x="95" y="74" text-anchor="middle" font-size="12" fill="#085041">Supervisado</text>
    </g>
    <line x1="155" y1="108" x2="110" y2="88" stroke="#9FE1CB" stroke-width="1"/>

    <g class="node" onclick="showPanel('no-supervisado')">
      <rect x="165" y="52" width="130" height="36" rx="6" fill="#9FE1CB"/>
      <text x="230" y="74" text-anchor="middle" font-size="12" fill="#085041">No supervisado</text>
    </g>
    <line x1="210" y1="108" x2="225" y2="88" stroke="#9FE1CB" stroke-width="1"/>

    <!-- Sub-nodes DL -->
    <g class="node" onclick="showPanel('rnn')">
      <rect x="440" y="52" width="80" height="36" rx="6" fill="#B5D4F4"/>
      <text x="480" y="74" text-anchor="middle" font-size="12" fill="#0C447C">RNN</text>
    </g>
    <line x1="490" y1="108" x2="480" y2="88" stroke="#B5D4F4" stroke-width="1"/>

    <g class="node" onclick="showPanel('cnn')">
      <rect x="535" y="52" width="80" height="36" rx="6" fill="#B5D4F4"/>
      <text x="575" y="74" text-anchor="middle" font-size="12" fill="#0C447C">CNN</text>
    </g>
    <line x1="555" y1="108" x2="570" y2="88" stroke="#B5D4F4" stroke-width="1"/>

    <!-- Sub-nodes NLP -->
    <g class="node" onclick="showPanel('gpt')">
      <rect x="50" y="365" width="90" height="34" rx="6" fill="#F5C4B3"/>
      <text x="95" y="386" text-anchor="middle" font-size="12" fill="#4A1B0C">GPT / LLMs</text>
    </g>
    <line x1="120" y1="347" x2="95" y2="365" stroke="#F5C4B3" stroke-width="1"/>

    <!-- Sub-nodes CV -->
    <g class="node" onclick="showPanel('yolo')">
      <rect x="555" y="365" width="90" height="34" rx="6" fill="#F4C0D1"/>
      <text x="600" y="386" text-anchor="middle" font-size="12" fill="#4B1528">YOLO / GAN</text>
    </g>
    <line x1="580" y1="347" x2="600" y2="365" stroke="#F4C0D1" stroke-width="1"/>

    <!-- Legend -->
    <rect x="10" y="460" width="12" height="12" rx="2" fill="#534AB7"/>
    <text x="27" y="472" font-size="11" fill="#5F5E5A">Concepto central</text>
    <rect x="130" y="460" width="12" height="12" rx="2" fill="#1D9E75"/>
    <text x="147" y="472" font-size="11" fill="#5F5E5A">Rama principal</text>
    <rect x="250" y="460" width="12" height="12" rx="2" fill="#9FE1CB"/>
    <text x="267" y="472" font-size="11" fill="#5F5E5A">Subconcepto</text>
  </svg>

  <p class="hint"><i class="ti ti-hand-click" aria-hidden="true"></i> Toca un nodo para ver detalles, descripción y recursos</p>

  <div id="info-panel" style="display:none"></div>
</div>

<script>
const data = {
  ia: {
    title:"Inteligencia Artificial",
    color:"#534AB7",
    icon:"ti-brain",
    badge:"Concepto central",
    badgeColor:"#EEEDFE",
    badgeText:"#534AB7",
    desc:"La Inteligencia Artificial (IA) es la rama de las ciencias de la computación que busca crear sistemas capaces de realizar tareas que normalmente requieren inteligencia humana: razonamiento, aprendizaje, percepción y toma de decisiones. Surge en la década de 1950 con Alan Turing y ha evolucionado hasta convertirse en el motor de la transformación digital global.",
    links:[
      {label:"¿Qué es la IA? – IBM",url:"https://www.ibm.com/es-es/topics/artificial-intelligence",icon:"ti-external-link"},
      {label:"Historia de la IA – Britannica",url:"https://www.britannica.com/technology/artificial-intelligence",icon:"ti-book"},
      {label:"Video intro IA – YouTube",url:"https://www.youtube.com/watch?v=ad79nYk2keg",icon:"ti-player-play"},
    ]
  },
  ml: {
    title:"Machine Learning",
    color:"#1D9E75",
    icon:"ti-chart-dots",
    badge:"Rama principal",
    badgeColor:"#E1F5EE",
    badgeText:"#0F6E56",
    desc:"El Aprendizaje Automático (ML) es un subcampo de la IA en el que los sistemas aprenden de los datos sin ser programados explícitamente. Los modelos identifican patrones estadísticos y mejoran su rendimiento con la experiencia. Se divide en aprendizaje supervisado, no supervisado y por refuerzo.",
    links:[
      {label:"ML explicado – Google",url:"https://developers.google.com/machine-learning/crash-course",icon:"ti-external-link"},
      {label:"Curso ML – Coursera",url:"https://www.coursera.org/learn/machine-learning",icon:"ti-school"},
      {label:"ML en 5 minutos – YouTube",url:"https://www.youtube.com/watch?v=ukzFI9rgwfU",icon:"ti-player-play"},
    ]
  },
  dl: {
    title:"Deep Learning",
    color:"#185FA5",
    icon:"ti-topology-star-3",
    badge:"Rama principal",
    badgeColor:"#E6F1FB",
    badgeText:"#185FA5",
    desc:"El Aprendizaje Profundo usa redes neuronales artificiales con múltiples capas para modelar representaciones abstractas de los datos. Es la tecnología detrás del reconocimiento de voz, traducción automática, generación de imágenes y los grandes modelos de lenguaje (LLMs).",
    links:[
      {label:"Deep Learning – MIT",url:"https://deeplearning.mit.edu/",icon:"ti-school"},
      {label:"Neural Networks – 3Blue1Brown",url:"https://www.youtube.com/watch?v=aircAruvnKk",icon:"ti-player-play"},
      {label:"Fast.ai (curso práctico)",url:"https://www.fast.ai/",icon:"ti-external-link"},
    ]
  },
  nlp: {
    title:"Procesamiento del Lenguaje Natural",
    color:"#993C1D",
    icon:"ti-message-language",
    badge:"Rama principal",
    badgeColor:"#FAECE7",
    badgeText:"#993C1D",
    desc:"El NLP (Natural Language Processing) permite que las máquinas comprendan, interpreten y generen texto humano. Incluye tareas como análisis de sentimientos, traducción automática, resumen de textos y chatbots. Los modelos Transformer como BERT y GPT han revolucionado este campo.",
    links:[
      {label:"NLP Overview – Stanford",url:"https://nlp.stanford.edu/",icon:"ti-school"},
      {label:"Transformers explicados",url:"https://huggingface.co/learn/nlp-course/chapter1/1",icon:"ti-external-link"},
      {label:"Video NLP – YouTube",url:"https://www.youtube.com/watch?v=CMrHM8a3hqw",icon:"ti-player-play"},
    ]
  },
  cv: {
    title:"Visión Computacional",
    color:"#993556",
    icon:"ti-eye",
    badge:"Rama principal",
    badgeColor:"#FBEAF0",
    badgeText:"#993556",
    desc:"La Visión Computacional permite a las máquinas interpretar y analizar imágenes y vídeos. Aplicaciones: diagnóstico médico por imágenes, vehículos autónomos, reconocimiento facial y control de calidad industrial. Usa redes convolucionales (CNN) y modelos generativos (GAN).",
    links:[
      {label:"CV con OpenCV – Docs",url:"https://opencv.org/",icon:"ti-external-link"},
      {label:"Computer Vision – fast.ai",url:"https://course.fast.ai/",icon:"ti-school"},
      {label:"Video: ¿Cómo ven las IA?",url:"https://www.youtube.com/watch?v=HcVFBJHkdUE",icon:"ti-player-play"},
    ]
  },
  etica: {
    title:"Ética e Impacto Social",
    color:"#BA7517",
    icon:"ti-scale",
    badge:"Transversal",
    badgeColor:"#FAEEDA",
    badgeText:"#854F0B",
    desc:"El desarrollo de la IA plantea desafíos éticos críticos: sesgos algorítmicos, privacidad, transparencia (IA explicable), desplazamiento laboral y responsabilidad en decisiones automatizadas. Organismos como la UNESCO y la UE trabajan en marcos regulatorios para una IA responsable.",
    links:[
      {label:"Ética IA – UNESCO",url:"https://www.unesco.org/es/artificial-intelligence/recommendation-ethics",icon:"ti-external-link"},
      {label:"AI Act – Unión Europea",url:"https://artificialintelligenceact.eu/",icon:"ti-file-certificate"},
      {label:"Video: Sesgos en IA",url:"https://www.youtube.com/watch?v=59bMh59JQDo",icon:"ti-player-play"},
    ]
  },
  supervisado:{
    title:"Aprendizaje Supervisado",
    color:"#0F6E56",
    icon:"ti-list-check",
    badge:"Subconcepto ML",
    badgeColor:"#E1F5EE",
    badgeText:"#0F6E56",
    desc:"Algoritmos entrenados con datos etiquetados (entrada → salida conocida). Ejemplos: regresión lineal, árboles de decisión, SVM, redes neuronales. Aplicaciones: detección de spam, clasificación de imágenes, predicción de precios.",
    links:[
      {label:"Supervised Learning – Google",url:"https://developers.google.com/machine-learning/crash-course/supervised-learning",icon:"ti-external-link"},
    ]
  },
  "no-supervisado":{
    title:"Aprendizaje No Supervisado",
    color:"#0F6E56",
    icon:"ti-topology-ring",
    badge:"Subconcepto ML",
    badgeColor:"#E1F5EE",
    badgeText:"#0F6E56",
    desc:"El modelo encuentra patrones en datos sin etiquetas. Técnicas: clustering (K-means), reducción de dimensionalidad (PCA), autoencoders. Útil para segmentación de clientes y detección de anomalías.",
    links:[
      {label:"Unsupervised – IBM",url:"https://www.ibm.com/es-es/topics/unsupervised-learning",icon:"ti-external-link"},
    ]
  },
  rnn:{
    title:"Redes Neuronales Recurrentes (RNN)",
    color:"#185FA5",
    icon:"ti-rotate-clockwise",
    badge:"Subconcepto DL",
    badgeColor:"#E6F1FB",
    badgeText:"#185FA5",
    desc:"Arquitectura diseñada para datos secuenciales (texto, audio, series temporales). Variantes como LSTM y GRU resuelven el problema del desvanecimiento del gradiente. Base de los primeros traductores automáticos neuronales.",
    links:[
      {label:"RNN – Colah's Blog",url:"https://colah.github.io/posts/2015-08-Understanding-LSTMs/",icon:"ti-external-link"},
    ]
  },
  cnn:{
    title:"Redes Convolucionales (CNN)",
    color:"#185FA5",
    icon:"ti-grid-dots",
    badge:"Subconcepto DL",
    badgeColor:"#E6F1FB",
    badgeText:"#185FA5",
    desc:"Arquitectura especializada en procesamiento de imágenes. Usa capas convolucionales para detectar características visuales jerárquicas (bordes → texturas → objetos). Modelos icónicos: AlexNet, VGG, ResNet.",
    links:[
      {label:"CNN Guide – Stanford CS231n",url:"https://cs231n.github.io/",icon:"ti-school"},
    ]
  },
  gpt:{
    title:"GPT y Modelos de Lenguaje Grande",
    color:"#993C1D",
    icon:"ti-robot",
    badge:"Subconcepto NLP",
    badgeColor:"#FAECE7",
    badgeText:"#993C1D",
    desc:"Los LLMs (Large Language Models) como GPT-4, Claude y Gemini son modelos de lenguaje masivos entrenados con billones de tokens. Capaces de generar texto, código, razonar y mantener conversaciones complejas mediante arquitectura Transformer.",
    links:[
      {label:"GPT-4 – OpenAI",url:"https://openai.com/gpt-4",icon:"ti-external-link"},
      {label:"¿Qué son los LLMs?",url:"https://www.youtube.com/watch?v=zjkBMFhNj_g",icon:"ti-player-play"},
    ]
  },
  yolo:{
    title:"YOLO y GAN",
    color:"#993556",
    icon:"ti-scan",
    badge:"Subconcepto CV",
    badgeColor:"#FBEAF0",
    badgeText:"#993556",
    desc:"YOLO (You Only Look Once) es un algoritmo de detección de objetos en tiempo real. Las GAN (Generative Adversarial Networks) generan imágenes sintéticas realistas a partir de ruido aleatorio. Ambos son pilares de la visión computacional moderna.",
    links:[
      {label:"YOLO – Ultralytics",url:"https://ultralytics.com/yolo",icon:"ti-external-link"},
      {label:"GAN explicado – YouTube",url:"https://www.youtube.com/watch?v=8L11aMN5KY8",icon:"ti-player-play"},
    ]
  },
};

function showPanel(id){
  const d=data[id]; if(!d) return;
  const p=document.getElementById('info-panel');
  p.style.display='block';
  p.innerHTML=`<div class="panel">
    <div class="panel-title">
      <i class="ti ${d.icon}" style="font-size:20px;color:${d.color}" aria-hidden="true"></i>
      ${d.title}
      <span class="badge" style="background:${d.badgeColor};color:${d.badgeText}">${d.badge}</span>
      <button class="close-btn" onclick="document.getElementById('info-panel').style.display='none'" aria-label="Cerrar">
        <i class="ti ti-x" aria-hidden="true"></i>
      </button>
    </div>
    <p class="panel-desc">${d.desc}</p>
    <div class="links-grid">
      ${d.links.map(l=>`<a class="link-card" href="${l.url}" target="_blank">
        <i class="ti ${l.icon}" style="color:${d.color}" aria-hidden="true"></i>
        <span>${l.label}</span>
      </a>`).join('')}
    </div>
  </div>`;
  p.scrollIntoView({behavior:'smooth',block:'nearest'});
}
</script>
