--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    galaxy_type character varying(40),
    galaxy_size integer,
    name character varying(40) NOT NULL,
    age_in_millions_of_years numeric(4,1),
    num_stars_in_billions integer
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(40),
    moon_type character varying(20),
    moon_shape character varying(20),
    planet_id integer NOT NULL
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(40),
    planet_shape character varying(20),
    star_id integer NOT NULL,
    is_spherical boolean,
    hosts_life boolean,
    planet_type text,
    num_moons integer
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(40),
    major_gas character varying(40),
    color character varying(20),
    galaxy_id integer NOT NULL
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: starplanet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.starplanet (
    star_id integer NOT NULL,
    planet_id integer NOT NULL,
    link character varying(20) NOT NULL,
    name character varying(20),
    starplanet_id integer NOT NULL
);


ALTER TABLE public.starplanet OWNER TO freecodecamp;

--
-- Name: starplanet_sp_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.starplanet_sp_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.starplanet_sp_id_seq OWNER TO freecodecamp;

--
-- Name: starplanet_sp_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.starplanet_sp_id_seq OWNED BY public.starplanet.starplanet_id;


--
-- Name: starplanet starplanet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.starplanet ALTER COLUMN starplanet_id SET DEFAULT nextval('public.starplanet_sp_id_seq'::regclass);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Dusty', NULL, 'Yuyuyu', 432.6, 5);
INSERT INTO public.galaxy VALUES (2, 'Shiny', NULL, 'Milkymon', 133.7, 7);
INSERT INTO public.galaxy VALUES (3, 'Abstract', NULL, 'Tracatyxl', 123.2, 2);
INSERT INTO public.galaxy VALUES (4, 'Satiny', NULL, 'Mitosjzys', 623.2, 9);
INSERT INTO public.galaxy VALUES (5, 'Emptiness', NULL, 'Beron', 928.1, 1);
INSERT INTO public.galaxy VALUES (6, 'Plasticular', NULL, 'Qwertyxy', 251.1, 5);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'Moon', 'Pretty', 'Sphere', 1);
INSERT INTO public.moon VALUES (2, 'Europa', 'Pretentious', 'Sphere', 5);
INSERT INTO public.moon VALUES (3, 'Mlonog', 'Snot', 'Oblong', 10);
INSERT INTO public.moon VALUES (4, 'ABA', 'S', 'Cylinder', 11);
INSERT INTO public.moon VALUES (5, 'Po', 'SS', 'Cyl', 10);
INSERT INTO public.moon VALUES (7, 'Qe', 'SS', 'Sphere', 10);
INSERT INTO public.moon VALUES (8, 'Tr', 'SS', 'Sphere', 11);
INSERT INTO public.moon VALUES (9, 'Yt', 'SS', 'Sphere', 12);
INSERT INTO public.moon VALUES (10, 'Un', 'SS', 'Sphere', 12);
INSERT INTO public.moon VALUES (11, 'Nb', 'SS', 'Sphere', 5);
INSERT INTO public.moon VALUES (12, 'Mp', 'SS', 'Sphere', 6);
INSERT INTO public.moon VALUES (13, 'Et', 'SS', 'Sphere', 8);
INSERT INTO public.moon VALUES (14, 'Ro', 'SS', 'Sphere', 12);
INSERT INTO public.moon VALUES (6, 'Wr', 'TR', 'Square', 10);
INSERT INTO public.moon VALUES (15, 'Vb', 'Crap', 'Square', 6);
INSERT INTO public.moon VALUES (16, 'Zg', 'Yuck', 'Rhombus', 10);
INSERT INTO public.moon VALUES (17, 'Rr', 'Yuck', 'Parallelogram', 10);
INSERT INTO public.moon VALUES (18, 'Db', 'Pretty', 'Rhombus', 10);
INSERT INTO public.moon VALUES (19, 'Ht', 'Pretentious', 'Circle', 10);
INSERT INTO public.moon VALUES (20, 'Jt', 'Snot', 'Cylinder', 10);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Earth', 'Round', 1, true, true, 'big blue', 1);
INSERT INTO public.planet VALUES (2, 'Venus', 'Round', 1, true, false, 'yellow acidy', 0);
INSERT INTO public.planet VALUES (3, 'Mercury', 'Round', 1, true, false, 'Rockey burnt', 0);
INSERT INTO public.planet VALUES (4, 'Mars', 'Round', 1, true, false, 'Rocky red', 0);
INSERT INTO public.planet VALUES (11, 'Gragan', 'Triangle', 4, true, false, 'Pointy', 2);
INSERT INTO public.planet VALUES (9, 'Pluto', 'Round', 1, true, false, 'ITS A PLANET!!', 0);
INSERT INTO public.planet VALUES (10, 'Cebatacus', 'Square', 3, true, true, 'People fall off it', 9);
INSERT INTO public.planet VALUES (12, 'Mimino', 'Rhombus', 6, true, true, 'Picassoy', 3);
INSERT INTO public.planet VALUES (8, 'Saturn', 'Round with rings', 1, true, false, 'Ringy purple', 1);
INSERT INTO public.planet VALUES (5, 'Jupiter', 'Round with rings', 1, true, false, 'Ringy brown', 2);
INSERT INTO public.planet VALUES (7, 'Neptune', 'Round with rings', 1, true, false, 'Ringy blue', 0);
INSERT INTO public.planet VALUES (6, 'Uranus', 'Round with rings', 1, true, false, 'Ringy yellow', 2);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'Giganticus', 'Hydrogen', 'Orange', 2);
INSERT INTO public.star VALUES (2, 'Minoria', 'Helium', 'Yellow', 3);
INSERT INTO public.star VALUES (3, 'Remora', 'Astatine', 'Green', 5);
INSERT INTO public.star VALUES (4, 'Atomos', 'Radium', 'Red', 6);
INSERT INTO public.star VALUES (5, 'Ramuh', 'Boron', 'Blue', 1);
INSERT INTO public.star VALUES (6, 'Shivakakaka', 'Nitrogen', 'Cyan', 4);


--
-- Data for Name: starplanet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.starplanet VALUES (1, 2, 'Vegigan', 'VG', 1);
INSERT INTO public.starplanet VALUES (1, 1, 'Ergigan', 'EG', 2);
INSERT INTO public.starplanet VALUES (1, 3, 'Mergigan', 'MG', 3);
INSERT INTO public.starplanet VALUES (1, 4, 'Magigan', 'MaG', 4);


--
-- Name: starplanet_sp_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.starplanet_sp_id_seq', 4, true);


--
-- Name: galaxy galaxy_galaxy_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_galaxy_id_key UNIQUE (galaxy_id);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_moon_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_moon_id_key UNIQUE (moon_id);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: planet planet_planet_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_planet_id_key UNIQUE (planet_id);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: star star_star_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_star_id_key UNIQUE (star_id);


--
-- Name: starplanet starplanet_link_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.starplanet
    ADD CONSTRAINT starplanet_link_key UNIQUE (link);


--
-- Name: starplanet starplanet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.starplanet
    ADD CONSTRAINT starplanet_pkey PRIMARY KEY (starplanet_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- Name: starplanet starplanet_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.starplanet
    ADD CONSTRAINT starplanet_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: starplanet starplanet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.starplanet
    ADD CONSTRAINT starplanet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- PostgreSQL database dump complete
--

