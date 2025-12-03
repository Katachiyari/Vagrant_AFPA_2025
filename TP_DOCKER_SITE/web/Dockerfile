# web/Dockerfile
# Utilise l'image officielle PHP 8.2 avec Apache pré-installé comme base
FROM php:8.2-apache

# Installation des extensions PHP requises (PDO, MySQL)
# Installe les extensions PHP pour communiquer avec MySQL/MariaDB
RUN docker-php-ext-install pdo pdo_mysql mysqli

# Activation du mod_rewrite pour Apache (optionnel mais utile)
# Active le module rewrite d'Apache (utile pour les URL rewriting, ex: .htaccess)
RUN a2enmod rewrite
