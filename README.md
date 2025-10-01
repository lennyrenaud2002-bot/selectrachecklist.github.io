<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Checklist Commerciale - Selectra</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="app-background">
        <div class="sidebar-container">
            <!-- Header -->
            <div class="sidebar-header">
                <h1 class="logo">⚡ SELECTRA</h1>
                <div class="call-timer">
                    <span id="timer-display">00:00</span>
                </div>
            </div>

            <!-- Checklist Sections -->
            <div class="checklist-content">
                
                <!-- Section Informations Client -->
                <section class="checklist-section">
                    <h3 class="section-title">📝 Informations Client</h3>
                    <div class="section-counter">
                        <span id="client-counter">0/8</span>
                    </div>
                    <div class="checklist-items">
                        <label class="checkbox-item required">
                            <input type="checkbox" id="nom" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">Nom collecté</span>
                            <span class="required-badge">*</span>
                        </label>
                        <label class="checkbox-item required">
                            <input type="checkbox" id="prenom" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">Prénom collecté</span>
                            <span class="required-badge">*</span>
                        </label>
                        <label class="checkbox-item required">
                            <input type="checkbox" id="adresse" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">Adresse complète</span>
                            <span class="required-badge">*</span>
                        </label>
                        <label class="checkbox-item required">
                            <input type="checkbox" id="email" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">Email valide</span>
                            <span class="required-badge">*</span>
                        </label>
                        <label class="checkbox-item required">
                            <input type="checkbox" id="telephone" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">Téléphone confirmé</span>
                            <span class="required-badge">*</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="pdl" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">PDL électricité (14 chiffres)</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="pce" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">PCE gaz (14 chiffres)</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="iban" data-section="client">
                            <span class="checkmark"></span>
                            <span class="item-text">IBAN sécurisé</span>
                        </label>
                    </div>
                </section>

                <!-- Section Accords Explicites -->
                <section class="checklist-section">
                    <h3 class="section-title">✅ Accords Explicites</h3>
                    <div class="section-counter">
                        <span id="accords-counter">0/7</span>
                    </div>
                    <div class="checklist-items">
                        <label class="checkbox-item required">
                            <input type="checkbox" id="rgpd" data-section="accords">
                            <span class="checkmark"></span>
                            <span class="item-text">RGPD données</span>
                            <span class="required-badge">OBLIGATOIRE</span>
                        </label>
                        <label class="checkbox-item required">
                            <input type="checkbox" id="reseau" data-section="accords">
                            <span class="checkmark"></span>
                            <span class="item-text">Accès réseau Enedis/GRDF</span>
                            <span class="required-badge">OBLIGATOIRE</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="voltalis" data-section="accords">
                            <span class="checkmark"></span>
                            <span class="item-text">Voltalis RDV planifié</span>
                        </label>
                        <label class="checkbox-item payant">
                            <input type="checkbox" id="axa" data-section="accords" data-payant="true">
                            <span class="checkmark"></span>
                            <span class="item-text">AXA Assistance 6,99€</span>
                            <span class="payant-badge">Payant</span>
                        </label>
                        <label class="checkbox-item payant">
                            <input type="checkbox" id="carbone" data-section="accords" data-payant="true">
                            <span class="checkmark"></span>
                            <span class="item-text">Compensation Carbone</span>
                            <span class="payant-badge">Payant</span>
                        </label>
                        <label class="checkbox-item payant">
                            <input type="checkbox" id="protected" data-section="accords" data-payant="true">
                            <span class="checkmark"></span>
                            <span class="item-text">Protected 14,99€</span>
                            <span class="payant-badge">Payant</span>
                        </label>
                        <label class="checkbox-item payant">
                            <input type="checkbox" id="mcp" data-section="accords" data-payant="true">
                            <span class="checkmark"></span>
                            <span class="item-text">Mon Conseiller Perso</span>
                            <span class="payant-badge">Payant</span>
                        </label>
                    </div>
                    <div class="validation-alert" id="payant-alert">
                        ⚠️ Minimum 2 services payants requis
                    </div>
                </section>

                <!-- Section Mentions Légales -->
                <section class="checklist-section">
                    <h3 class="section-title">⚖️ Mentions Légales</h3>
                    <div class="section-counter">
                        <span id="mentions-counter">0/6</span>
                    </div>
                    <div class="checklist-items">
                        <label class="checkbox-item timer-item">
                            <input type="checkbox" id="axa_exclusions" data-section="mentions" data-timer="30">
                            <span class="checkmark"></span>
                            <span class="item-text">AXA 4 exclusions lues (30s min)</span>
                            <span class="timer-badge" id="timer-axa_exclusions">0s</span>
                        </label>
                        <label class="checkbox-item timer-item">
                            <input type="checkbox" id="axa_rgpd" data-section="mentions" data-timer="20">
                            <span class="checkmark"></span>
                            <span class="item-text">AXA RGPD + durée (20s min)</span>
                            <span class="timer-badge" id="timer-axa_rgpd">0s</span>
                        </label>
                        <label class="checkbox-item timer-item">
                            <input type="checkbox" id="carbone_mention" data-section="mentions" data-timer="15">
                            <span class="checkmark"></span>
                            <span class="item-text">Carbone processus (15s min)</span>
                            <span class="timer-badge" id="timer-carbone_mention">0s</span>
                        </label>
                        <label class="checkbox-item timer-item">
                            <input type="checkbox" id="protected_mention" data-section="mentions" data-timer="15">
                            <span class="checkmark"></span>
                            <span class="item-text">Protected 30j rétractation (15s min)</span>
                            <span class="timer-badge" id="timer-protected_mention">0s</span>
                        </label>
                        <label class="checkbox-item required">
                            <input type="checkbox" id="frais_mes" data-section="mentions">
                            <span class="checkmark"></span>
                            <span class="item-text">Frais MES communiqués</span>
                            <span class="required-badge">OBLIGATOIRE</span>
                        </label>
                        <label class="checkbox-item required">
                            <input type="checkbox" id="retractation" data-section="mentions">
                            <span class="checkmark"></span>
                            <span class="item-text">Délai rétractation 14j</span>
                            <span class="required-badge">OBLIGATOIRE</span>
                        </label>
                    </div>
                </section>

                <!-- Section Signatures SMS -->
                <section class="checklist-section">
                    <h3 class="section-title">📱 Signatures SMS</h3>
                    <div class="section-counter">
                        <span id="sms-counter">0/4</span>
                    </div>
                    <div class="checklist-items">
                        <label class="checkbox-item">
                            <input type="checkbox" id="sms_axa" data-section="sms">
                            <span class="checkmark"></span>
                            <span class="item-text">Code AXA reçu/validé</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="sms_carbone" data-section="sms">
                            <span class="checkmark"></span>
                            <span class="item-text">Code Carbone reçu/validé</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="sms_protected" data-section="sms">
                            <span class="checkmark"></span>
                            <span class="item-text">Code Protected reçu/validé</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="sms_mcp" data-section="sms">
                            <span class="checkmark"></span>
                            <span class="item-text">Code MCP reçu/validé</span>
                        </label>
                    </div>
                </section>

                <!-- Section Étapes Commerciales -->
                <section class="checklist-section">
                    <h3 class="section-title">🎯 Étapes Commerciales</h3>
                    <div class="section-counter">
                        <span id="etapes-counter">0/7</span>
                    </div>
                    <div class="checklist-items">
                        <label class="checkbox-item">
                            <input type="checkbox" id="qualification" data-section="etapes">
                            <span class="checkmark"></span>
                            <span class="item-text">Client qualifié correctement</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="besoins" data-section="etapes">
                            <span class="checkmark"></span>
                            <span class="item-text">Besoins analysés</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="offre" data-section="etapes">
                            <span class="checkmark"></span>
                            <span class="item-text">Offre présentée clairement</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="objections" data-section="etapes">
                            <span class="checkmark"></span>
                            <span class="item-text">Objections traitées</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="addons" data-section="etapes">
                            <span class="checkmark"></span>
                            <span class="item-text">Add-ons proposés (min 2 payants)</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="signatures" data-section="etapes">
                            <span class="checkmark"></span>
                            <span class="item-text">Signatures obtenues</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" id="recap" data-section="etapes">
                            <span class="checkmark"></span>
                            <span class="item-text">Récap final effectué</span>
                        </label>
                    </div>
                </section>

                <!-- Section Notes d'Appel -->
                <section class="checklist-section">
                    <h3 class="section-title">📋 Notes d'Appel</h3>
                    <div class="notes-area">
                        <textarea 
                            id="notes" 
                            placeholder="Observations importantes, objections client, remarques..."
                            rows="4"
                        ></textarea>
                    </div>
                </section>

                <!-- Section Résumé -->
                <section class="checklist-section summary-section">
                    <h3 class="section-title">📊 Résumé</h3>
                    <div class="summary-grid">
                        <div class="summary-item">
                            <span class="summary-label">Accords validés</span>
                            <span class="summary-value" id="summary-accords">0/7</span>
                        </div>
                        <div class="summary-item">
                            <span class="summary-label">Services payants</span>
                            <span class="summary-value" id="summary-payants">0/4</span>
                        </div>
                        <div class="summary-item">
                            <span class="summary-label">Mentions légales</span>
                            <span class="summary-value" id="summary-mentions">0/6</span>
                        </div>
                        <div class="summary-item">
                            <span class="summary-label">Étapes complètes</span>
                            <span class="summary-value" id="summary-etapes">0/7</span>
                        </div>
                    </div>
                    <div class="export-section">
                        <button class="btn btn--primary export-btn" id="export-btn">
                            📄 Exporter le résumé
                        </button>
                    </div>
                </section>

            </div>
        </div>
    </div>

    <script src="app.js"></script>
</body>
</html>
