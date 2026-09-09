SYNAPSO FUSION BRIDGE 0.1.0 - WINDOWS / PYTHON 3.14
=====================================================

Installation automatique
-------------------------
1. Fermez Autodesk Fusion 360.
2. Extrayez completement le fichier ZIP.
3. Double-cliquez sur INSTALLER_FUSION.cmd.
4. Relancez Fusion 360.
5. Dans Fusion : Utilitaires > Complements > Scripts et complements.
6. Verifiez que SynapsoFusionBridge est charge.

Le programme d'installation copie uniquement l'add-in dans votre profil Autodesk et cree
un secret aleatoire local dans %LOCALAPPDATA%\Synapso\bridge-secret. Il n'affiche pas ce secret.

Installation manuelle
---------------------
Copiez le dossier SynapsoFusionBridge dans :
%APPDATA%\Autodesk\Autodesk Fusion 360\API\AddIns\SynapsoFusionBridge

Le paquet contient Pydantic et pydantic-core compiles pour le Python 3.14 integre a la version
de Fusion detectee le 9 septembre 2026. Une autre version majeure/mineure de Python Fusion
necessitera un paquet correspondant.

Test
----
Quand l'add-in fonctionne, son service local repond uniquement sur 127.0.0.1:17861 et exige
le secret local. Le relais Synapso utilise automatiquement le meme fichier secret.

Pour le parcours serveur complet, le relais desktop doit aussi etre lance et le serveur doit
etre passe en FUSION_MODE=fusion. Laissez le serveur en mode mock avant cette etape.
