<script lang="ts">
  import Bloc from "../lib/components/Bloc.svelte";
</script>

<div class="bloc-title">
  <h2>/ Bloc 1 Gérer le patrimoine informatique</h2>
</div>
<div class="bloc1">
  <div class="border">
    <Bloc
      competences="Compétence 1 - Recenser et identifier les ressources numériques"
      projectTitle="Installation et configuration de GLPI"
      date="Octobre 2025"
      contexte="Réalisation:"
    />
    <p>
      Dans le cadre des travaux pratiques associés à l'unité d'enseignement
      Support et mise à disposition de services informatiques, il a été procédé
      au déploiement d'une solution GLPI sur une machine virtuelle fonctionnant
      sous Debian, dans le but d'automatiser le recensement des ressources
      matérielles et logicielles (postes de travail, serveurs, périphériques) et
      d'en centraliser la gestion au sein d'une interface web unifiée.
    </p>
    <p class="section-title">1. Prérequis système</p>
    <ul class="tp-list">
      <li>Serveur web Apache2</li>
      <li>Système de gestion de base de données MariaDB</li>
      <li>
        PHP 8.x accompagné des extensions requises : curl, gd, mbstring, xml,
        zip, intl, mysql
      </li>
    </ul>

    <p class="section-title">2. Installation de l'environnement (Debian)</p>
    <pre><span
        ># Mise à jour du système
apt update && apt upgrade -y

# Installation d'Apache, PHP et de ses extensions
apt install apache2 mariadb-server -y
apt install php libapache2-mod-php php-mysql php-curl php-gd php-intl php-zip php-xml php-mbstring -y

# Activation du service Apache au démarrage du système
systemctl enable apache2
systemctl start apache2

# Procédure de sécurisation de MariaDB

mysql_secure_installation</span
      ></pre>

    <p class="section-title">3. Configuration de la base de données</p>
    <pre><span>mysql -u root -p</span>
 
<span class="hl"
        >CREATE DATABASE glpi CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;</span
      >
<span class="hl"
        >CREATE USER 'glpi'@'localhost' IDENTIFIED BY 'mot_de_passe_securise';</span
      >
<span class="hl"
        >GRANT ALL PRIVILEGES ON glpi.* TO 'glpi'@'localhost';
FLUSH PRIVILEGES;
EXIT;</span
      ></pre>

    <p class="section-title">4. Installation de GLPI</p>
    <pre><span
        >wget https://github.com/glpi-project/glpi/releases/download/10.0.15/glpi-10.0.15.tgz 
cd /var/www/html/ </span>
 
<span>tar -xvzf glpi-10.0.15.tgz</span>
 
<span>chown -R www-data:www-data glpi</span>
<span>chmod -R 755 glpi</span>
 
<span>a2enmod rewrite</span>
<span>systemctl restart apache2</span></pre>

    <p>
      La finalisation de l'installation s'effectue par le biais de l'interface
      web disponible à l'adresse <code
        ><span> http://IP_SERVEUR/glpi</span></code
      >. Il convient, lors de cette étape, de renseigner les paramètres de
      connexion à la base de données préalablement configurée. À l'issue de
      cette procédure, le répertoire <code>/install</code> est supprimé afin d'éliminer
      tout vecteur de vulnérabilité potentielle.
    </p>

    <p class="section-title">5. Mise en place de l'inventaire automatique</p>
    <p>
      Afin d'assurer la collecte automatisée des informations matérielles et
      logicielles des équipements du parc informatique, la configuration de
      l'agent GLPI Inventory a été réalisée selon les étapes suivantes :
    </p>
    <ul class="tp-list">
      <li>
        Activation du plugin GLPI Inventory via la Marketplace de l'application.
      </li>
      <li>
        Déploiement de l'agent GLPI sur l'ensemble des postes clients concernés.
      </li>
      <li>
        Définition du serveur cible au sein de la configuration de l'agent :
      </li>
    </ul>
    <pre><span>glpi-agent --server http://IP_SERVEUR/glpi</span></pre>

    <p>
      Une fois le déploiement effectué, les équipements remontent
      automatiquement leurs informations dans la console GLPI, comprenant
      notamment :
    </p>
    <ul class="tp-list">
      <li>
        Caractéristiques matérielles (processeur, mémoire vive, capacité de
        stockage)
      </li>
      <li>Inventaire des logiciels installés</li>
      <li>Adresse IP et paramètres réseau associés</li>
      <li>Numéros de série et état courant du matériel</li>
    </ul>
  </div>
</div>

<div class="bloc1">
  <div class="border">
    <Bloc
      competences="Compétence 2 - Exploiter des référentiels, normes et standards adoptés par le prestataire informatique"
      projectTitle="Configuration des règles de gestion des incidents dans GLPI selon le référentiel ITIL"
      date="Octobre 2025"
      contexte="Réalisation:"
    />
    <p>
      Dans le cadre des travaux pratiques associés à l'unité d'enseignement
      Support et mise à disposition de services informatiques, il a été procédé
      à la configuration d'une instance GLPI en appliquant les bonnes pratiques
      du référentiel ITIL, afin de structurer la gestion des incidents au sein
      d'une entreprise fictive. L'objectif était de mettre en place un système
      de ticketing cohérent avec les standards adoptés par les prestataires
      informatiques professionnels.
    </p>

    <p class="section-title">1. Compréhension du référentiel ITIL</p>
    <p>
      ITIL (Information Technology Infrastructure Library) est un ensemble de
      bonnes pratiques destinées à la gestion des services informatiques. Dans
      le cadre de ce TP, les concepts suivants ont été appliqués :
    </p>
    <ul class="tp-list">
      <li>
        <strong>Gestion des incidents</strong> : traitement structuré des dysfonctionnements
        affectant les utilisateurs
      </li>
      <li>
        <strong>Niveaux de priorité</strong> : classification des incidents selon
        leur urgence et leur impact
      </li>
      <li>
        <strong>Catégorisation</strong> : organisation des tickets par type de problème
        afin d'en faciliter le traitement
      </li>
    </ul>

    <p class="section-title">2. Configuration des niveaux de priorité</p>
    <p>
      Quatre niveaux de priorité ont été définis dans GLPI, conformément à la
      matrice urgence/impact préconisée par ITIL :
    </p>
    <ul class="tp-list">
      <li>
        <strong>Très haute</strong> : incident bloquant tout ou partie de l'activité
        de l'entreprise, nécessitant une intervention immédiate
      </li>
      <li>
        <strong>Haute</strong> : impact fort sur un service ou un groupe d'utilisateurs,
        traitement prioritaire requis
      </li>
      <li>
        <strong>Moyenne</strong> : gêne notable pour l'utilisateur, mais poursuite
        de l'activité possible
      </li>
      <li>
        <strong>Basse</strong> : incident mineur sans conséquence immédiate sur la
        productivité
      </li>
    </ul>

    <p class="section-title">3. Création des cas d'incidents types</p>
    <p>
      Des modèles d'incidents représentatifs des situations courantes en
      entreprise ont été créés et associés à un niveau de priorité adapté :
    </p>
    <ul class="tp-list">
      <li>
        <strong>Panne réseau</strong> : perte de connectivité affectant un ou
        plusieurs postes de travail — priorité <em>Très haute</em>
      </li>
      <li>
        <strong>Accès refusé à un logiciel</strong> : impossibilité pour un
        utilisateur d'accéder à une application métier — priorité <em>Haute</em>
      </li>
    </ul>
    <p>
      Chaque incident a été catégorisé et rattaché à un niveau de priorité afin
      d'assurer un traitement rapide et conforme aux bonnes pratiques du
      référentiel ITIL.
    </p>
  </div>
</div>

<style>
  .bloc-title {
    display: flex;
    max-width: 1000px;
    margin: 0 auto;
  }

  h2 {
    font-family: var(--sfpro);
  }
  .bloc1 {
    display: flex;
    justify-content: center;
  }

  .border {
    border: 1px, solid;
    padding: 10px 10px;
    padding-top: 0px;
    border-radius: 7px;
    max-width: 1000px;
  }
  p {
    margin-top: 0px;
    margin-bottom: 10px;
    font-family: var(--sfpro);
  }
  li {
    font-family: var(--sfpro);
  }
  .section-title {
    font-weight: 800;
  }
  span {
    background-color: var(--indigo-500);
  }
</style>
