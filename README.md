***Descrição do projeto:***

Banco de dados relacional utilizando MariaDB no ambiente XAMPP, com foco em comandos SQL essenciais para o gerenciamento de alunos em uma instituição de ensino.


***Instruções para phpmyadmin***

-- phpMyAdmin SQL Dump
-- version 5.2.1
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Oct 02, 2025 at 11:58 PM
-- Server version: 10.4.32-MariaDB
-- PHP Version: 8.2.12

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `escola`
--

-- --------------------------------------------------------

--
-- Table structure for table `alunos`
--

CREATE TABLE `alunos` (
  `id` int(11) NOT NULL,
  `nome` varchar(100) DEFAULT NULL,
  `email` varchar(100) DEFAULT NULL,
  `data_nascimento` date DEFAULT NULL,
  `curso` varchar(50) DEFAULT NULL,
  `ativo` tinyint(1) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `alunos`
--

INSERT INTO `alunos` (`id`, `nome`, `email`, `data_nascimento`, `curso`, `ativo`) VALUES
(1, 'João Silva', 'joao.silva@email.com', '2000-05-12', 'Engenharia', 1),
(2, 'Mariana Costa', 'mariana.costa@email.com', '1999-11-20', 'Direito', 1),
(3, 'Pedro Oliveira', 'pedro.oliveira@email.com', '2001-01-30', 'Administração', 0),
(4, 'Ana Pereira', 'ana.pereira@email.com', '1998-08-05', 'Engenharia', 1),
(5, 'Lucas Almeida', 'lucas.almeida@email.com', '2002-03-15', 'Design', 1);

--
-- Indexes for dumped tables
--

--
-- Indexes for table `alunos`
--
ALTER TABLE `alunos`
  ADD PRIMARY KEY (`id`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `alunos`
--
ALTER TABLE `alunos`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;


***Exemplo de comandos SQL***

-- Exemplos de consultas
-- SELECT * FROM alunos;
-- SELECT * FROM alunos WHERE ativo = TRUE;
-- SELECT * FROM alunos WHERE curso = 'Engenharia';
-- SELECT * FROM alunos ORDER BY nome ASC;

-- Exemplo de atualização:
-- UPDATE alunos SET curso = 'Marketing' WHERE id = 3;

-- Exemplo de exclusão:
-- DELETE FROM alunos WHERE id = 4;
