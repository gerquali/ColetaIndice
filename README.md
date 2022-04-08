# ColetaIndice
Coleta índices do site investing.com e alimenta em base de dados
######################################################
#                    Requsitos                       #
######################################################

## Debian/Ubuntu
apt install python python3-pip

## Redhat/Fedora
yum install python python3-pip

## Módulos Python
pip install mysql-connector-python	
pip install playwright
playwright install
playwright install-deps

######################################################
#                      MySQL                         #
######################################################

## Cria o schema
create database forex;
use forex;

## Cria as tabelas
CREATE TABLE `TB_compra` (
  `ID` int NOT NULL AUTO_INCREMENT,
  `AOA` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `EUR` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `BRL` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `Data` datetime NOT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

CREATE TABLE `TB_venda` (
  `ID` int NOT NULL AUTO_INCREMENT,
  `AOA` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `EUR` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `BRL` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `Data` datetime NOT NULL,
  PRIMARY KEY (`ID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

