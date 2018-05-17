# it-pro-- phpMyAdmin SQL Dump
-- version 4.7.7
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: May 17, 2018 at 04:18 AM
-- Server version: 10.1.30-MariaDB
-- PHP Version: 7.2.2

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `pos`
--

-- --------------------------------------------------------

--
-- Table structure for table `cart`
--

CREATE TABLE `cart` (
  `cartid` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `productid` int(11) NOT NULL,
  `qty` double NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Table structure for table `category`
--

CREATE TABLE `category` (
  `categoryid` int(11) NOT NULL,
  `category_name` varchar(30) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `category`
--

INSERT INTO `category` (`categoryid`, `category_name`) VALUES
(1, 'OUTDOOR SPORTS'),
(2, 'INDOOR SPORTS'),
(3, 'WATER SPORTS');

-- --------------------------------------------------------

--
-- Table structure for table `customer`
--

CREATE TABLE `customer` (
  `userid` int(11) NOT NULL,
  `customer_name` varchar(50) NOT NULL,
  `address` varchar(150) NOT NULL,
  `contact` varchar(50) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `customer`
--

INSERT INTO `customer` (`userid`, `customer_name`, `address`, `contact`) VALUES
(2, 'Neovic Devierte', 'Silay City, Negros Occidental', '09092735719');

-- --------------------------------------------------------

--
-- Table structure for table `inventory`
--

CREATE TABLE `inventory` (
  `inventoryid` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `action` varchar(50) NOT NULL,
  `productid` int(11) NOT NULL,
  `quantity` double NOT NULL,
  `inventory_date` datetime NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `inventory`
--

INSERT INTO `inventory` (`inventoryid`, `userid`, `action`, `productid`, `quantity`, `inventory_date`) VALUES
(1, 2, 'Purchase', 4, 10, '2017-09-18 09:32:01'),
(2, 2, 'Purchase', 20, 10, '2017-09-18 09:32:01'),
(3, 2, 'Purchase', 1, 99, '2017-09-18 09:32:01'),
(4, 2, 'Purchase', 2, 20, '2017-09-18 09:32:01'),
(5, 2, 'Purchase', 2, 10, '2017-09-18 09:34:29'),
(6, 2, 'Purchase', 2, 10, '2017-09-18 11:09:21'),
(7, 2, 'Purchase', 3, 12, '2017-09-18 11:09:22'),
(8, 2, 'Purchase', 4, 8, '2017-09-18 11:09:22'),
(9, 1, 'Add Product', 27, 10, '2017-09-18 13:59:25'),
(10, 1, 'Update quantity', 27, 20, '2017-09-18 14:04:32'),
(11, 2, 'Purchase', 3, 1, '2018-04-28 12:40:18'),
(12, 4, 'Add Product', 28, 10, '2018-04-28 12:43:30'),
(13, 2, 'Purchase', 28, 1, '2018-04-28 12:44:09'),
(14, 1, 'Add Product', 29, 10, '2018-04-28 15:41:08'),
(15, 2, 'Purchase', 29, 1, '2018-04-28 15:41:57'),
(16, 2, 'Purchase', 1, 2, '2018-05-01 17:13:54'),
(17, 4, 'Add Product', 30, 100, '2018-05-01 17:21:57'),
(18, 2, 'Purchase', 1, 1, '2018-05-03 18:21:04'),
(19, 2, 'Purchase', 2, 2, '2018-05-06 09:12:21'),
(20, 12, 'Purchase', 1, 1, '2018-05-06 09:51:52'),
(21, 4, 'Add Product', 31, 3, '2018-05-14 12:55:06'),
(22, 17, 'Purchase', 31, 3, '2018-05-14 12:56:26'),
(23, 16, 'Purchase', 22, 3, '2018-05-15 15:25:05'),
(24, 4, 'Add Product', 32, 50, '2018-05-15 16:17:47'),
(25, 4, 'Add Product', 33, 50, '2018-05-15 16:18:59'),
(26, 4, 'Add Product', 34, 50, '2018-05-15 16:19:34'),
(27, 4, 'Add Product', 35, 50, '2018-05-15 16:19:59'),
(28, 4, 'Add Product', 36, 50, '2018-05-15 16:20:26'),
(29, 4, 'Add Product', 37, 50, '2018-05-15 16:20:43'),
(30, 4, 'Add Product', 38, 50, '2018-05-15 16:21:13'),
(31, 4, 'Add Product', 39, 50, '2018-05-15 16:21:30'),
(32, 4, 'Add Product', 40, 50, '2018-05-15 16:22:26'),
(33, 4, 'Add Product', 41, 50, '2018-05-15 16:22:46'),
(34, 4, 'Add Product', 42, 50, '2018-05-15 16:23:05'),
(35, 4, 'Add Product', 43, 50, '2018-05-15 16:23:20'),
(36, 4, 'Add Product', 44, 50, '2018-05-15 16:24:15'),
(37, 4, 'Add Product', 45, 50, '2018-05-15 16:24:54'),
(38, 4, 'Add Product', 46, 50, '2018-05-15 16:25:10'),
(39, 4, 'Add Product', 47, 50, '2018-05-15 16:25:34'),
(40, 4, 'Add Product', 48, 50, '2018-05-15 16:26:01'),
(41, 16, 'Purchase', 34, 2, '2018-05-15 22:58:02'),
(42, 16, 'Purchase', 41, 3, '2018-05-15 22:58:47'),
(43, 16, 'Purchase', 44, 6, '2018-05-15 22:59:58'),
(44, 16, 'Purchase', 34, 3, '2018-05-15 23:01:19'),
(45, 18, 'Purchase', 33, 10, '2018-05-15 23:12:31'),
(46, 18, 'Purchase', 41, 10, '2018-05-15 23:13:11'),
(47, 18, 'Purchase', 33, 2, '2018-05-15 23:15:51'),
(48, 18, 'Purchase', 33, 4, '2018-05-15 23:55:59'),
(49, 18, 'Purchase', 39, 10, '2018-05-16 00:10:44'),
(50, 18, 'Purchase', 35, 20, '2018-05-16 00:10:44'),
(51, 18, 'Purchase', 32, 1, '2018-05-16 00:10:44'),
(52, 19, 'Purchase', 42, 10, '2018-05-16 00:30:33'),
(53, 19, 'Purchase', 40, 10, '2018-05-16 00:30:33'),
(54, 19, 'Purchase', 48, 10, '2018-05-16 00:32:15'),
(55, 19, 'Purchase', 47, 20, '2018-05-16 00:32:15'),
(56, 20, 'Purchase', 41, 19, '2018-05-16 14:43:11'),
(57, 20, 'Purchase', 35, 15, '2018-05-16 14:43:11'),
(58, 4, 'Add Product', 49, 50, '2018-05-16 14:45:17'),
(59, 4, 'Add Product', 50, 100, '2018-05-16 16:04:25'),
(60, 4, 'Add Product', 51, 100, '2018-05-16 16:05:28'),
(61, 4, 'Add Product', 52, 100, '2018-05-16 16:07:20'),
(62, 4, 'Add Product', 53, 100, '2018-05-16 16:09:06'),
(63, 4, 'Add Product', 54, 100, '2018-05-16 16:09:43'),
(64, 4, 'Add Product', 55, 100, '2018-05-16 16:10:56'),
(65, 4, 'Add Product', 56, 100, '2018-05-16 16:11:51'),
(66, 4, 'Add Product', 57, 100, '2018-05-16 16:12:26'),
(67, 4, 'Add Product', 58, 100, '2018-05-16 16:13:00'),
(68, 4, 'Add Product', 59, 100, '2018-05-16 16:13:57'),
(69, 4, 'Add Product', 60, 100, '2018-05-16 16:15:29'),
(70, 4, 'Add Product', 61, 100, '2018-05-16 16:16:26'),
(71, 4, 'Add Product', 62, 100, '2018-05-16 16:16:57'),
(72, 4, 'Add Product', 63, 100, '2018-05-16 16:17:52'),
(73, 4, 'Add Product', 64, 100, '2018-05-16 16:18:43'),
(74, 4, 'Add Product', 65, 100, '2018-05-16 16:19:16'),
(75, 4, 'Add Product', 66, 100, '2018-05-16 16:21:12'),
(76, 4, 'Add Product', 67, 100, '2018-05-16 16:21:43'),
(77, 4, 'Add Product', 68, 100, '2018-05-16 16:22:44'),
(78, 4, 'Add Product', 69, 100, '2018-05-16 16:23:31'),
(79, 4, 'Add Product', 70, 100, '2018-05-16 16:25:52'),
(80, 4, 'Add Product', 71, 100, '2018-05-16 16:26:45'),
(81, 4, 'Add Product', 72, 100, '2018-05-16 16:27:12'),
(82, 4, 'Add Product', 73, 100, '2018-05-16 16:27:50'),
(83, 4, 'Add Product', 74, 100, '2018-05-16 16:28:23'),
(84, 4, 'Add Product', 75, 100, '2018-05-16 16:29:21'),
(85, 4, 'Add Product', 76, 100, '2018-05-16 16:29:57'),
(86, 4, 'Add Product', 77, 100, '2018-05-16 16:30:53'),
(87, 4, 'Add Product', 78, 100, '2018-05-16 16:31:28'),
(88, 4, 'Add Product', 79, 100, '2018-05-16 16:32:26'),
(89, 20, 'Purchase', 52, 4, '2018-05-16 16:50:06'),
(90, 20, 'Purchase', 63, 2, '2018-05-16 16:50:07'),
(91, 4, 'Add Product', 80, 5000, '2018-05-16 17:27:01'),
(92, 4, 'Add Product', 81, 50, '2018-05-16 17:28:18'),
(93, 4, 'Add Product', 82, 50, '2018-05-16 17:29:15'),
(94, 4, 'Add Product', 83, 10, '2018-05-16 17:30:07'),
(95, 4, 'Add Product', 84, 10, '2018-05-16 17:30:45'),
(96, 4, 'Add Product', 85, 10, '2018-05-16 17:31:20'),
(97, 4, 'Add Product', 86, 10, '2018-05-16 17:31:44'),
(98, 4, 'Add Product', 87, 10, '2018-05-16 17:32:14'),
(99, 4, 'Add Product', 88, 10, '2018-05-16 17:32:42'),
(100, 4, 'Add Product', 89, 10, '2018-05-16 17:33:18'),
(101, 4, 'Add Product', 90, 10, '2018-05-16 17:34:03'),
(102, 4, 'Add Product', 91, 10, '2018-05-16 17:34:31'),
(103, 4, 'Add Product', 92, 10, '2018-05-16 17:34:56'),
(104, 4, 'Add Product', 93, 10, '2018-05-16 17:35:31'),
(105, 4, 'Add Product', 94, 10, '2018-05-16 17:36:04'),
(106, 21, 'Purchase', 82, 4, '2018-05-16 17:37:56'),
(107, 4, 'Add Product', 95, 100, '2018-05-17 07:11:28'),
(108, 4, 'Add Product', 96, 100, '2018-05-17 07:12:55'),
(109, 4, 'Add Product', 97, 100, '2018-05-17 07:13:22'),
(110, 4, 'Add Product', 98, 100, '2018-05-17 07:13:48'),
(111, 4, 'Add Product', 99, 100, '2018-05-17 07:14:15'),
(112, 4, 'Add Product', 100, 100, '2018-05-17 07:14:56'),
(113, 4, 'Add Product', 101, 100, '2018-05-17 07:15:25'),
(114, 4, 'Add Product', 102, 100, '2018-05-17 07:17:28'),
(115, 4, 'Add Product', 103, 100, '2018-05-17 07:18:11'),
(116, 4, 'Add Product', 104, 100, '2018-05-17 07:18:37'),
(117, 4, 'Add Product', 105, 100, '2018-05-17 07:19:04'),
(118, 4, 'Add Product', 106, 100, '2018-05-17 07:19:41'),
(119, 4, 'Add Product', 107, 100, '2018-05-17 07:20:07'),
(120, 4, 'Add Product', 108, 100, '2018-05-17 07:20:36'),
(121, 4, 'Add Product', 109, 100, '2018-05-17 07:21:08'),
(122, 4, 'Add Product', 110, 100, '2018-05-17 07:21:42'),
(123, 4, 'Add Product', 111, 100, '2018-05-17 07:22:19'),
(124, 4, 'Add Product', 112, 100, '2018-05-17 07:22:48'),
(125, 4, 'Add Product', 113, 100, '2018-05-17 07:23:17'),
(126, 4, 'Add Product', 114, 100, '2018-05-17 07:23:46'),
(127, 4, 'Add Product', 115, 100, '2018-05-17 07:24:15'),
(128, 4, 'Add Product', 116, 100, '2018-05-17 07:25:11'),
(129, 4, 'Add Product', 117, 100, '2018-05-17 07:25:39'),
(130, 4, 'Add Product', 118, 100, '2018-05-17 07:26:08'),
(131, 4, 'Add Product', 119, 100, '2018-05-17 07:26:48'),
(132, 4, 'Add Product', 120, 100, '2018-05-17 07:27:14'),
(133, 4, 'Add Product', 121, 100, '2018-05-17 07:27:50'),
(134, 4, 'Add Product', 122, 100, '2018-05-17 07:28:25'),
(135, 4, 'Add Product', 123, 100, '2018-05-17 07:29:04'),
(136, 4, 'Add Product', 124, 100, '2018-05-17 07:29:32'),
(137, 4, 'Add Product', 125, 100, '2018-05-17 07:30:10');

-- --------------------------------------------------------

--
-- Table structure for table `product`
--

CREATE TABLE `product` (
  `productid` int(11) NOT NULL,
  `categoryid` int(11) NOT NULL,
  `product_name` varchar(150) NOT NULL,
  `product_price` double NOT NULL,
  `product_qty` double NOT NULL,
  `photo` varchar(200) NOT NULL,
  `supplierid` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `product`
--

INSERT INTO `product` (`productid`, `categoryid`, `product_name`, `product_price`, `product_qty`, `photo`, `supplierid`) VALUES
(95, 1, 'SG CRICKET BAT', 2000, 100, 'upload/sg cobra_1526521336.jpg', 4),
(96, 1, 'GRAY-NICOLIS CRICKET BAT', 2500, 100, 'upload/graynicolis_1526521375.jpg', 4),
(97, 1, 'KOOKABURRA CRICKET BAT', 3000, 100, 'upload/kookaburra_1526521402.jpg', 4),
(98, 1, 'SPARTAN CRICKET BAT', 5000, 100, 'upload/Spartan-Steel-Cricket-Bat_1526521428.jpg', 4),
(99, 1, 'MRF CRICKET BAT', 2500, 100, 'upload/mrf bats_1526521455.jpg', 4),
(100, 1, 'SG CRICKET HELMET', 1000, 100, 'upload/sg glove_1526521496.jpg', 4),
(101, 1, 'GRAY-NICOLIS CRICKET HELMET', 1000, 100, 'upload/graynicolis helmet_1526521525.jpg', 4),
(102, 1, 'SG ELBOW GUARD', 900, 100, 'upload/elbow guard_1526521648.jpg', 4),
(103, 1, 'SG CRICKET GLOVES', 1200, 100, 'upload/sg gloves_1526521691.jpg', 4),
(104, 1, 'GM CRICKET GLOVES', 1300, 100, 'upload/GM-606-Gloves_1526521717.jpg', 4),
(105, 1, 'SPARTAN CRICKET GLOVES', 2000, 100, 'upload/spartan gloves_1526521744.jpg', 4),
(106, 1, 'SG CRICKET PADS', 2200, 100, 'upload/sg pads_1526521781.jpg', 4),
(107, 1, 'SPARTAN CRICKET PADS', 2700, 100, 'upload/spartan pads_1526521807.jpg', 4),
(108, 1, 'SG CRICKET THIGH PADS', 1500, 100, 'upload/sg thigh pad_1526521836.jpg', 4),
(109, 1, 'SS CRICKET THIGH PADS', 1000, 100, 'upload/ss thigh pad_1526521868.jpg', 4),
(110, 1, 'ADIDAS CRICKET SHOES', 2500, 100, 'upload/adidas shoes_1526521901.jpg', 4),
(111, 1, 'ADIDAS FOOTBALL SHOES', 4000, 100, 'upload/football aadidas shoes_1526521938.jpg', 4),
(112, 1, 'NIKE FOOTBALL SHOES', 3500, 100, 'upload/football shoes_1526521968.jpg', 4),
(113, 1, 'ADIDAS KNEE PADS', 4000, 100, 'upload/knee pads_1526521997.jpg', 4),
(114, 1, 'KOOKABURRA CRICKET BAL', 2000, 100, 'upload/kookaburra balls_1526522026.jpg', 4),
(115, 1, 'PUMA CRICKET BALL', 1900, 100, 'upload/puma ball_1526522055.jpg', 4),
(116, 3, 'SHOULDER GUARD ICE HOCKEY', 5000, 100, 'upload/Shoulder-Pad-Sizing_1526522111.png', 4),
(117, 3, 'HELMET ICE HOCKEY', 3700, 100, 'upload/icehockey helmet_1526522139.jpg', 4),
(118, 3, 'BAT ICE HOCKEY', 4560, 100, 'upload/icehockey bats_1526522168.jpg', 4),
(119, 3, 'SWIMMING GOGGLES ADIDAS', 2800, 100, 'upload/adidas googles_1526522208.jpg', 4),
(120, 3, 'SWIMMING GOGGLES NIKE', 2400, 100, 'upload/nike googles_1526522234.jpg', 4),
(121, 3, 'SWIMMING CAP ADIDAS', 3200, 100, 'upload/adidas caps_1526522270.jpg', 4),
(122, 3, 'SWIMMING CAP NIKE', 3100, 100, 'upload/nike caps_1526522305.jpg', 4),
(123, 2, 'CHESS BOARD', 500, 100, 'upload/chess board_1526522344.jpg', 4),
(124, 2, 'CARROM BOARD', 750, 100, 'upload/carrom boaard_1526522372.jpg', 4),
(125, 2, 'YONEX BADMINTON RACKET', 1000, 100, 'upload/yonex bats_1526522410.jpg', 4);

-- --------------------------------------------------------

--
-- Table structure for table `sales`
--

CREATE TABLE `sales` (
  `salesid` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `sales_total` double NOT NULL,
  `sales_date` datetime NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `sales`
--

INSERT INTO `sales` (`salesid`, `userid`, `sales_total`, `sales_date`) VALUES
(1, 2, 34, '2017-09-16 16:23:38'),
(2, 2, 18, '2017-09-16 16:25:28'),
(3, 2, 6, '2017-09-16 16:27:31'),
(4, 2, 1014244, '2017-09-16 16:44:01'),
(5, 2, 9588, '2017-09-18 09:06:29'),
(6, 2, 88779, '2017-09-18 09:08:42'),
(7, 2, 15579, '2017-09-18 09:09:34'),
(8, 2, 112361, '2017-09-18 09:32:00'),
(9, 2, 7990, '2017-09-18 09:34:29'),
(10, 2, 18370, '2017-09-18 11:09:21'),
(11, 2, 599, '2018-04-28 12:40:17'),
(12, 2, 41000, '2018-04-28 12:44:09'),
(13, 2, 15422, '2018-04-28 15:41:57'),
(14, 2, 1798, '2018-05-01 17:13:53'),
(15, 2, 899, '2018-05-03 18:21:03'),
(16, 2, 1598, '2018-05-06 09:12:20'),
(17, 12, 899, '2018-05-06 09:51:52'),
(18, 17, 135, '2018-05-14 12:56:26'),
(19, 16, 0, '2018-05-15 15:24:25'),
(20, 16, 1857, '2018-05-15 15:25:04'),
(21, 16, 60, '2018-05-15 22:58:02'),
(22, 16, 60, '2018-05-15 22:58:47'),
(23, 16, 0, '2018-05-15 22:59:05'),
(24, 16, 180, '2018-05-15 22:59:58'),
(25, 16, 0, '2018-05-15 23:00:04'),
(26, 16, 90, '2018-05-15 23:01:19'),
(27, 18, 400, '2018-05-15 23:12:30'),
(28, 18, 200, '2018-05-15 23:13:11'),
(29, 18, 80, '2018-05-15 23:15:51'),
(30, 18, 160, '2018-05-15 23:55:58'),
(31, 18, 2100, '2018-05-16 00:10:44'),
(32, 19, 500, '2018-05-16 00:30:33'),
(33, 19, 3000, '2018-05-16 00:32:15'),
(34, 20, 1130, '2018-05-16 14:43:11'),
(35, 20, 17600, '2018-05-16 16:50:06'),
(36, 20, 0, '2018-05-16 16:51:49'),
(37, 21, 36360, '2018-05-16 17:37:56');

-- --------------------------------------------------------

--
-- Table structure for table `sales_detail`
--

CREATE TABLE `sales_detail` (
  `sales_detailid` int(11) NOT NULL,
  `salesid` int(11) NOT NULL,
  `productid` int(11) NOT NULL,
  `sales_qty` double NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `sales_detail`
--

INSERT INTO `sales_detail` (`sales_detailid`, `salesid`, `productid`, `sales_qty`) VALUES
(1, 2, 1, 12),
(2, 2, 2, 10),
(3, 3, 3, 11),
(4, 4, 2, 50),
(5, 4, 1, 106),
(6, 4, 5, 1000),
(7, 5, 2, 12),
(8, 6, 5, 101),
(9, 7, 1, 10),
(10, 7, 3, 11),
(11, 8, 4, 10),
(12, 8, 20, 10),
(13, 8, 1, 99),
(14, 8, 2, 20),
(15, 9, 2, 10),
(16, 10, 2, 10),
(17, 10, 3, 12),
(18, 10, 4, 8),
(19, 11, 3, 1),
(20, 12, 28, 1),
(21, 13, 29, 1),
(22, 14, 1, 2),
(23, 15, 1, 1),
(24, 16, 2, 2),
(25, 17, 1, 1),
(26, 18, 31, 3),
(27, 20, 22, 3),
(28, 21, 34, 2),
(29, 22, 41, 3),
(30, 24, 44, 6),
(31, 26, 34, 3),
(32, 27, 33, 10),
(33, 28, 41, 10),
(34, 29, 33, 2),
(35, 30, 33, 4),
(36, 31, 39, 10),
(37, 31, 35, 20),
(38, 31, 32, 1),
(39, 32, 42, 10),
(40, 32, 40, 10),
(41, 33, 48, 10),
(42, 33, 47, 20),
(43, 34, 41, 19),
(44, 34, 35, 15),
(45, 35, 52, 4),
(46, 35, 63, 2),
(47, 37, 82, 4);

-- --------------------------------------------------------

--
-- Table structure for table `supplier`
--

CREATE TABLE `supplier` (
  `userid` int(11) NOT NULL,
  `company_name` varchar(50) NOT NULL,
  `company_address` varchar(150) NOT NULL,
  `contact` varchar(50) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `supplier`
--

INSERT INTO `supplier` (`userid`, `company_name`, `company_address`, `contact`) VALUES
(4, 'TS SPORTS', 'ROAD NO: 4,MADHAPUR ,HYDERABAD,TELANGANA,560002', '8903456819');

-- --------------------------------------------------------

--
-- Table structure for table `user`
--

CREATE TABLE `user` (
  `userid` int(11) NOT NULL,
  `username` varchar(30) NOT NULL,
  `password` varchar(50) NOT NULL,
  `access` int(1) NOT NULL DEFAULT '2'
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `user`
--

INSERT INTO `user` (`userid`, `username`, `password`, `access`) VALUES
(1, 'admin', '21232f297a57a5a743894a0e4a801fc3', 1),
(2, 'user', 'ee11cbb19052e40b07aac0ca060c23ee', 2),
(4, 'supplier', '99b0e8da24e29e4ccb5d7d76e677c2ac', 3),
(5, 'madu', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(6, 'madu1', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(7, 'madu', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(8, 'madu2', '46f94c8de14fb36680850768ff1b7f2a', 2),
(9, 'madu342', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(10, 'madu543', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(11, 'raju', '03c017f682085142f3b60f56673e22dc', 2),
(12, 'abcd', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(13, 'abcd', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(14, 'supplier', '99b0e8da24e29e4ccb5d7d76e677c2ac', 2),
(15, 'supplier', '99b0e8da24e29e4ccb5d7d76e677c2ac', 2),
(16, 'madhu', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(17, 'pab', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(18, 'nad', '202cb962ac59075b964b07152d234b70', 2),
(19, 'abc', '202cb962ac59075b964b07152d234b70', 2),
(20, 'sai', '81dc9bdb52d04dc20036dbd8313ed055', 2),
(21, 'OM', '827ccb0eea8a706c4c34a16891f84e7b', 2);

--
-- Indexes for dumped tables
--

--
-- Indexes for table `cart`
--
ALTER TABLE `cart`
  ADD PRIMARY KEY (`cartid`);

--
-- Indexes for table `category`
--
ALTER TABLE `category`
  ADD PRIMARY KEY (`categoryid`);

--
-- Indexes for table `customer`
--
ALTER TABLE `customer`
  ADD PRIMARY KEY (`userid`);

--
-- Indexes for table `inventory`
--
ALTER TABLE `inventory`
  ADD PRIMARY KEY (`inventoryid`);

--
-- Indexes for table `product`
--
ALTER TABLE `product`
  ADD PRIMARY KEY (`productid`);

--
-- Indexes for table `sales`
--
ALTER TABLE `sales`
  ADD PRIMARY KEY (`salesid`);

--
-- Indexes for table `sales_detail`
--
ALTER TABLE `sales_detail`
  ADD PRIMARY KEY (`sales_detailid`);

--
-- Indexes for table `supplier`
--
ALTER TABLE `supplier`
  ADD PRIMARY KEY (`userid`);

--
-- Indexes for table `user`
--
ALTER TABLE `user`
  ADD PRIMARY KEY (`userid`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `cart`
--
ALTER TABLE `cart`
  MODIFY `cartid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=14;

--
-- AUTO_INCREMENT for table `category`
--
ALTER TABLE `category`
  MODIFY `categoryid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=4;

--
-- AUTO_INCREMENT for table `inventory`
--
ALTER TABLE `inventory`
  MODIFY `inventoryid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=138;

--
-- AUTO_INCREMENT for table `product`
--
ALTER TABLE `product`
  MODIFY `productid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=126;

--
-- AUTO_INCREMENT for table `sales`
--
ALTER TABLE `sales`
  MODIFY `salesid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=38;

--
-- AUTO_INCREMENT for table `sales_detail`
--
ALTER TABLE `sales_detail`
  MODIFY `sales_detailid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=48;

--
-- AUTO_INCREMENT for table `user`
--
ALTER TABLE `user`
  MODIFY `userid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=22;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
