---
layout: project
title: WoW DataHub ☞ Game Management Dashboard & Analytics Platform
date: 2024-04-01
screenshot:
  src: /assets/img/projects/WoW/Homepage.png
  srcset:
    1920w: /assets/img/projects/WoW/Homepage.png
    960w: /assets/img/projects/WoW/Homepage@0.5x.png
    480w: /assets/img/projects/WoW/Homepage@0.25x.png
description: >
  A comprehensive database solution for MMORPG character data management, featuring:
    - Normalized relational database with optimized schema design
    - Robust ETL pipeline for automated data ingestion and transformation
    - Secure JAVA-based data access layer with SQL injection prevention
    - Complex analytics engine for multi-dimensional game statistics
    - Interactive web dashboard for stakeholder insights
links:
  - title: Repository
    url: https://github.com/YannaCS/WoW-DataHub
featured: true
--- 
<h2> Project Overview </h2>
<svg viewBox="0 0 1400 900" xmlns="http://www.w3.org/2000/svg">
  <!-- Background -->
  <rect width="1400" height="900" fill="#f8f9fa"/>
  
  <!-- Title -->
  <text x="700" y="40" font-size="28" font-weight="bold" text-anchor="middle" fill="#1a1a1a">WoW DataHub Complete System Workflow</text>
  
  <!-- User/Browser Section -->
  <g id="user-section">
    <rect x="50" y="80" width="250" height="350" fill="#e1f5fe" stroke="#0277bd" stroke-width="2" rx="10"/>
    <text x="175" y="110" font-size="20" font-weight="bold" text-anchor="middle" fill="#0277bd">User Browser</text>
    
    <!-- Web Pages -->
    <rect x="70" y="130" width="210" height="35" fill="#81d4fa" rx="5"/>
    <text x="175" y="152" font-size="13" text-anchor="middle">🏠 Home Dashboard</text>
    
    <rect x="70" y="175" width="210" height="35" fill="#81d4fa" rx="5"/>
    <text x="175" y="197" font-size="13" text-anchor="middle">🔍 Find Characters</text>
    
    <rect x="70" y="220" width="210" height="35" fill="#81d4fa" rx="5"/>
    <text x="175" y="242" font-size="13" text-anchor="middle">📋 Character Details</text>
    
    <rect x="70" y="265" width="210" height="35" fill="#81d4fa" rx="5"/>
    <text x="175" y="287" font-size="13" text-anchor="middle">⚔️ Weapon Update</text>
    
    <rect x="70" y="310" width="210" height="35" fill="#81d4fa" rx="5"/>
    <text x="175" y="332" font-size="13" text-anchor="middle">🔄 ETL Control</text>
    
    <!-- User Actions -->
    <text x="175" y="370" font-size="14" font-weight="bold" text-anchor="middle" fill="#0277bd">User Actions</text>
    <text x="175" y="390" font-size="11" text-anchor="middle">• View analytics</text>
    <text x="175" y="405" font-size="11" text-anchor="middle">• Search characters</text>
    <text x="175" y="420" font-size="11" text-anchor="middle">• Update equipment</text>
  </g>
  
  <!-- Web Application Section -->
  <g id="webapp-section">
    <rect x="350" y="80" width="300" height="750" fill="#fce4ec" stroke="#c2185b" stroke-width="2" rx="10"/>
    <text x="500" y="110" font-size="20" font-weight="bold" text-anchor="middle" fill="#c2185b">Web Application</text>
    <text x="500" y="130" font-size="12" text-anchor="middle" fill="#c2185b">Apache Tomcat + JSP</text>
    
    <!-- Servlets -->
    <g>
      <rect x="370" y="150" width="260" height="200" fill="#f8bbd0" rx="5"/>
      <text x="500" y="175" font-size="14" font-weight="bold" text-anchor="middle">Servlets (Controllers)</text>
      
      <rect x="380" y="190" width="240" height="25" fill="#f48fb1" rx="3"/>
      <text x="500" y="206" font-size="11" text-anchor="middle" fill="white">HomeController</text>
      
      <rect x="380" y="220" width="240" height="25" fill="#f48fb1" rx="3"/>
      <text x="500" y="236" font-size="11" text-anchor="middle" fill="white">FindCharacter</text>
      
      <rect x="380" y="250" width="240" height="25" fill="#f48fb1" rx="3"/>
      <text x="500" y="266" font-size="11" text-anchor="middle" fill="white">CharacterDetailReport</text>
      
      <rect x="380" y="280" width="240" height="25" fill="#f48fb1" rx="3"/>
      <text x="500" y="296" font-size="11" text-anchor="middle" fill="white">WeaponUpdate</text>
      
      <rect x="380" y="310" width="240" height="25" fill="#f48fb1" rx="3"/>
      <text x="500" y="326" font-size="11" text-anchor="middle" fill="white">ETLController</text>
    </g>
    
    <!-- Business Logic -->
    <g>
      <rect x="370" y="370" width="260" height="120" fill="#f8bbd0" rx="5"/>
      <text x="500" y="395" font-size="14" font-weight="bold" text-anchor="middle">Business Rules Service</text>
      
      <text x="380" y="415" font-size="10">✓ Character name uniqueness</text>
      <text x="380" y="430" font-size="10">✓ Weapon requirements</text>
      <text x="380" y="445" font-size="10">✓ Currency cap validation</text>
      <text x="380" y="460" font-size="10">✓ Job compatibility checks</text>
      <text x="380" y="475" font-size="10">✓ Equipment slot validation</text>
    </g>
    
    <!-- DAOs -->
    <g>
      <rect x="370" y="510" width="260" height="150" fill="#f8bbd0" rx="5"/>
      <text x="500" y="535" font-size="14" font-weight="bold" text-anchor="middle">Data Access Layer</text>
      
      <rect x="380" y="550" width="115" height="25" fill="#f48fb1" rx="3"/>
      <text x="437" y="566" font-size="10" text-anchor="middle" fill="white">PlayersDao</text>
      
      <rect x="505" y="550" width="115" height="25" fill="#f48fb1" rx="3"/>
      <text x="562" y="566" font-size="10" text-anchor="middle" fill="white">CharactersDao</text>
      
      <rect x="380" y="580" width="115" height="25" fill="#f48fb1" rx="3"/>
      <text x="437" y="596" font-size="10" text-anchor="middle" fill="white">WeaponsDao</text>
      
      <rect x="505" y="580" width="115" height="25" fill="#f48fb1" rx="3"/>
      <text x="562" y="596" font-size="10" text-anchor="middle" fill="white">InventoryDao</text>
      
      <rect x="380" y="610" width="115" height="25" fill="#f48fb1" rx="3"/>
      <text x="437" y="626" font-size="10" text-anchor="middle" fill="white">ViewsDao</text>
      
      <rect x="505" y="610" width="115" height="25" fill="#f48fb1" rx="3"/>
      <text x="562" y="626" font-size="10" text-anchor="middle" fill="white">CurrenciesDao</text>
      
      <text x="500" y="650" font-size="11" text-anchor="middle">+ 12 more DAOs</text>
    </g>
    
    <!-- JSP Views -->
    <g>
      <rect x="370" y="680" width="260" height="120" fill="#f8bbd0" rx="5"/>
      <text x="500" y="705" font-size="14" font-weight="bold" text-anchor="middle">JSP Views</text>
      
      <text x="380" y="725" font-size="10">• Home.jsp (Dashboard)</text>
      <text x="380" y="740" font-size="10">• FindCharacter.jsp</text>
      <text x="380" y="755" font-size="10">• CharacterDetailReport.jsp</text>
      <text x="380" y="770" font-size="10">• WeaponUpdate.jsp</text>
      <text x="380" y="785" font-size="10">• ETL.jsp</text>
    </g>
  </g>
  
  <!-- ETL Process Section -->
  <g id="etl-section">
    <rect x="700" y="450" width="280" height="380" fill="#f3e5f5" stroke="#7b1fa2" stroke-width="2" rx="10"/>
    <text x="840" y="480" font-size="18" font-weight="bold" text-anchor="middle" fill="#7b1fa2">ETL Process</text>
    
    <!-- Default Data ETL -->
    <g>
      <rect x="720" y="500" width="240" height="140" fill="#e1bee7" rx="5"/>
      <text x="840" y="520" font-size="13" font-weight="bold" text-anchor="middle">Default Data ETL</text>
      
      <text x="730" y="540" font-size="10">• 18 Clans (race mappings)</text>
      <text x="730" y="555" font-size="10">• 20 Statistics</text>
      <text x="730" y="570" font-size="10">• 20 Currencies</text>
      <text x="730" y="585" font-size="10">• 100+ Weapons</text>
      <text x="730" y="600" font-size="10">• 150+ Gears</text>
      <text x="730" y="615" font-size="10">• 100+ Consumables</text>
      <text x="730" y="630" font-size="10">• Item bonuses</text>
    </g>
    
    <!-- Dynamic Data ETL -->
    <g>
      <rect x="720" y="660" width="240" height="140" fill="#e1bee7" rx="5"/>
      <text x="840" y="680" font-size="13" font-weight="bold" text-anchor="middle">Dynamic Data ETL</text>
      
      <text x="730" y="700" font-size="10">• 50 Players</text>
      <text x="730" y="715" font-size="10">• 100 Characters</text>
      <text x="730" y="730" font-size="10">• Character wealth</text>
      <text x="730" y="745" font-size="10">• Job assignments</text>
      <text x="730" y="760" font-size="10">• Inventory items</text>
      <text x="730" y="775" font-size="10">• Equipped items</text>
      <text x="730" y="790" font-size="10">• Character stats</text>
    </g>
  </g>
  
  <!-- External API Section -->
  <g id="api-section">
    <rect x="700" y="80" width="280" height="180" fill="#e3f2fd" stroke="#1976d2" stroke-width="2" rx="10"/>
    <text x="840" y="110" font-size="18" font-weight="bold" text-anchor="middle" fill="#1976d2">Blizzard WoW API</text>
    
    <rect x="720" y="130" width="240" height="30" fill="#bbdefb" rx="5"/>
    <text x="840" y="150" font-size="12" text-anchor="middle">OAuth2 Authentication</text>
    
    <rect x="720" y="170" width="240" height="30" fill="#bbdefb" rx="5"/>
    <text x="840" y="190" font-size="12" text-anchor="middle">Realms & Characters</text>
    
    <rect x="720" y="210" width="240" height="30" fill="#bbdefb" rx="5"/>
    <text x="840" y="230" font-size="12" text-anchor="middle">Items & Equipment</text>
  </g>
  
  <!-- Database Section -->
  <g id="database-section">
    <rect x="1050" y="80" width="300" height="750" fill="#e8f5e9" stroke="#388e3c" stroke-width="2" rx="10"/>
    <text x="1200" y="110" font-size="20" font-weight="bold" text-anchor="middle" fill="#388e3c">MySQL Database</text>
    
    <!-- Core Tables -->
    <g>
      <rect x="1070" y="140" width="260" height="180" fill="#c8e6c9" rx="5"/>
      <text x="1200" y="165" font-size="14" font-weight="bold" text-anchor="middle">Core Tables (18)</text>
      
      <g transform="translate(1080, 180)">
        <rect x="0" y="0" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="55" y="17" font-size="10" text-anchor="middle">Players</text>
        
        <rect x="120" y="0" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="175" y="17" font-size="10" text-anchor="middle">Characters</text>
        
        <rect x="0" y="30" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="55" y="47" font-size="10" text-anchor="middle">Items</text>
        
        <rect x="120" y="30" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="175" y="47" font-size="10" text-anchor="middle">Weapons</text>
        
        <rect x="0" y="60" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="55" y="77" font-size="10" text-anchor="middle">Gears</text>
        
        <rect x="120" y="60" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="175" y="77" font-size="10" text-anchor="middle">Consumables</text>
        
        <rect x="0" y="90" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="55" y="107" font-size="10" text-anchor="middle">Inventory</text>
        
        <rect x="120" y="90" width="110" height="25" fill="#a5d6a7" rx="3"/>
        <text x="175" y="107" font-size="10" text-anchor="middle">Currencies</text>
      </g>
      
      <text x="1200" y="310" font-size="11" text-anchor="middle">+ 10 more tables</text>
    </g>
    
    <!-- Business Rules -->
    <g>
      <rect x="1070" y="340" width="260" height="160" fill="#c8e6c9" rx="5"/>
      <text x="1200" y="365" font-size="14" font-weight="bold" text-anchor="middle">Business Rule Triggers</text>
      
      <text x="1080" y="385" font-size="10">✓ enforce_currency_caps</text>
      <text x="1080" y="400" font-size="10">✓ enforce_stack_size</text>
      <text x="1080" y="415" font-size="10">✓ validate_equipment_slots</text>
      <text x="1080" y="430" font-size="10">✓ enforce_weapon_required</text>
      <text x="1080" y="445" font-size="10">✓ validate_job_progression</text>
      <text x="1080" y="460" font-size="10">✓ check_name_uniqueness</text>
      <text x="1080" y="475" font-size="10">✓ validate_race_clan</text>
      <text x="1080" y="490" font-size="10">✓ check_inventory_limits</text>
    </g>
    
    <!-- Analytics Views -->
    <g>
      <rect x="1070" y="520" width="260" height="180" fill="#c8e6c9" rx="5"/>
      <text x="1200" y="545" font-size="14" font-weight="bold" text-anchor="middle">Analytics Views (9)</text>
      
      <text x="1080" y="565" font-size="10">• OverallStatsView</text>
      <text x="1080" y="580" font-size="10">• DailyActivePlayersView</text>
      <text x="1080" y="595" font-size="10">• JobDistributionView</text>
      <text x="1080" y="610" font-size="10">• ClanDistributionView</text>
      <text x="1080" y="625" font-size="10">• CurrencyStatsView</text>
      <text x="1080" y="640" font-size="10">• ItemTypeDistributionView</text>
      <text x="1080" y="655" font-size="10">• TopPlayersByLevelView</text>
      <text x="1080" y="670" font-size="10">• TopPlayersByWealthView</text>
      <text x="1080" y="685" font-size="10">• CharacterInventoryDetailsView</text>
    </g>
    
    <!-- Constraints -->
    <g>
      <rect x="1070" y="720" width="260" height="80" fill="#81c784" rx="5"/>
      <text x="1200" y="745" font-size="13" font-weight="bold" text-anchor="middle">Constraints</text>
      <text x="1080" y="765" font-size="10">• Foreign keys (referential integrity)</text>
      <text x="1080" y="780" font-size="10">• Check constraints (data validation)</text>
      <text x="1080" y="795" font-size="10">• Unique constraints (no duplicates)</text>
    </g>
  </g>
  
  <!-- Connection Arrows -->
  <!-- User to Web App -->
  <path d="M 300 255 L 350 255" stroke="#0277bd" stroke-width="3" fill="none" marker-end="url(#arrowblue)"/>
  <text x="325" y="235" font-size="10" text-anchor="middle" fill="#0277bd">HTTP</text>
  <text x="325" y="245" font-size="10" text-anchor="middle" fill="#0277bd">Requests</text>
  
  <!-- Web App to User -->
  <path d="M 350 285 L 300 285" stroke="#c2185b" stroke-width="3" fill="none" marker-end="url(#arrowpink)"/>
  <text x="325" y="305" font-size="10" text-anchor="middle" fill="#c2185b">HTML</text>
  <text x="325" y="315" font-size="10" text-anchor="middle" fill="#c2185b">Response</text>
  
  <!-- Web App to Database -->
  <path d="M 650 400 L 1050 400" stroke="#388e3c" stroke-width="3" fill="none" marker-end="url(#arrowgreen)"/>
  <text x="880" y="390" font-size="11" text-anchor="middle" fill="#388e3c">JDBC Queries</text>
  
  <!-- Database to Web App -->
  <path d="M 1050 430 L 650 430" stroke="#388e3c" stroke-width="3" fill="none" marker-end="url(#arrowgreen)"/>
  <text x="800" y="440" font-size="11" text-anchor="middle" fill="#388e3c">Result Sets</text>
  
  <!-- Web App to ETL -->
  <path d="M 500 340 Q 500 640 700 640" stroke="#c2185b" stroke-width="3" fill="none" marker-end="url(#arrowpink)"/>
  <text x="680" y="655" font-size="10" text-anchor="middle" fill="#c2185b">Trigger</text>
  <text x="680" y="665" font-size="10" text-anchor="middle" fill="#c2185b">ETL</text>
  
  <!-- API to ETL -->
  <path d="M 840 260 L 840 450" stroke="#1976d2" stroke-width="3" fill="none" marker-end="url(#arrowblue)"/>
  <text x="860" y="355" font-size="10" fill="#1976d2">API Data</text>
  
  <!-- ETL to Database -->
  <path d="M 980 640 L 1050 640" stroke="#7b1fa2" stroke-width="3" fill="none" marker-end="url(#arrowpurple)"/>
  <text x="1015" y="630" font-size="10" text-anchor="middle" fill="#7b1fa2">Bulk Insert</text>
  
  <!-- Arrow definitions -->
  <defs>
    <marker id="arrowblue" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#0277bd"/>
    </marker>
    <marker id="arrowgreen" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#388e3c"/>
    </marker>
    <marker id="arrowpurple" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#7b1fa2"/>
    </marker>
    <marker id="arrowpink" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L0,6 L9,3 z" fill="#c2185b"/>
    </marker>
  </defs>
  
  <!-- Process Flow Key -->
  <g transform="translate(50, 480)">
    <rect x="0" y="0" width="250" height="150" fill="#f5f5f5" stroke="#666" rx="5"/>
    <text x="125" y="20" font-size="14" font-weight="bold" text-anchor="middle">System Flow</text>
    
    <text x="10" y="40" font-size="11" font-weight="bold">1. User Interaction:</text>
    <text x="20" y="55" font-size="10">Browse → Request → Response</text>
    
    <text x="10" y="75" font-size="11" font-weight="bold">2. Data Operations:</text>
    <text x="20" y="90" font-size="10">Servlet → DAO → Database</text>
    
    <text x="10" y="110" font-size="11" font-weight="bold">3. ETL Process:</text>
    <text x="20" y="125" font-size="10">API → Transform → Load</text>
  </g>
  
  <!-- Technology Stack -->
  <g transform="translate(50, 650)">
    <rect x="0" y="0" width="250" height="180" fill="#fff3e0" stroke="#ff6f00" rx="5"/>
    <text x="125" y="20" font-size="14" font-weight="bold" text-anchor="middle" fill="#ff6f00">Technology Stack</text>
    
    <text x="10" y="40" font-size="11" font-weight="bold">Frontend:</text>
    <text x="20" y="55" font-size="10">• JSP + Bootstrap 5</text>
    <text x="20" y="70" font-size="10">• Chart.js for analytics</text>
    
    <text x="10" y="90" font-size="11" font-weight="bold">Backend:</text>
    <text x="20" y="105" font-size="10">• Java 17 + Servlets</text>
    <text x="20" y="120" font-size="10">• Apache Tomcat 11</text>
    
    <text x="10" y="140" font-size="11" font-weight="bold">Database:</text>
    <text x="20" y="155" font-size="10">• MySQL 8.0</text>
    <text x="20" y="170" font-size="10">• JDBC connectivity</text>
  </g>
</svg>

<h3>Watch how it works:</h3>
<iframe 
    width="900" 
    height="506.25"
    src="https://www.youtube.com/embed/YLpJw_OEadc"
    frameborder="0" 
    allowfullscreen>
</iframe>


<h2> Development Process </h2>
<h3> Phase 1: Database Design & Schema Creation </h3>
Objective: Design normalized relational database schema with ER-Diagram for MMORPG character data

- Created comprehensive entity-relationship diagrams using crow's feet notation
- Normalized database to 3NF to eliminate redundancy and ensure data integrity
- Defined relationship modalities and cardinalities for optimal performance
- Technologies: **MySQL, ER Modeling, Database Normalization**

<img src="{{ '/assets/img/projects/WoW/ERD.jpg' | relative_url }}" alt='ER Diagram'>


<h3> Phase 2: Physical Implementation & Data Layer</h3>
Objective: Build secure data access layer with proper validation and abstraction

- Implemented physical data models with appropriate primary and foreign key, and update, delete constraints
- Developed JAVA-based data access layer using JDBC with prepared statements
- Created comprehensive input validation to prevent SQL injection attacks
- Built abstraction layers for database operations with transaction support
- Technologies: **JAVA, JDBC, Data Validation, SQL Security**

<h3> Phase 3: ETL Pipeline & Data Integration</h3>
Objective: Build robust ETL processes for data ingestion and transformation

- Designed automated ETL pipelines to extract data from multiple game servers
- Implemented data transformation rules for standardization and quality assurance
- Created incremental loading strategies for real-time data synchronization
- Built data validation and error handling mechanisms with detailed logging
- Developed error handling and logging mechanisms for failed data loads
- Technologies: **JAVA, JDBC Batch Processing, SQL Stored Procedures, Data Validation**

<img src="{{ '/assets/img/projects/WoW/etl.png' | relative_url }}" alt='' width="900">

<h3> Phase 4: Query Development & Analytics</h3>
Objective: Implement complex analytics and reporting capabilities  

- Developed sophisticated SQL queries using multiple joins and aggregations
- Created stored procedures for complex business logic and performance optimization
- Built analytics engine for multi-dimensional game statistics analysis
- Implemented efficient indexing strategies for query optimization
- Technologies: **SQL, Joins & Aggregations, Views, Data Analytics, Reporting**

<img src="{{ '/assets/img/projects/WoW/dbViews.png' | relative_url }}" alt='' width="300">

<h3> Phase 5: Web Interface & Stakeholder Dashboard</h3>
Objective: Create interactive web application for data visualization and management 

- Built JSP-based web application with MVC architecture
- Implemented dynamic filtering and search capabilities
- Created interactive charts and visualizations for game statistics
- Developed role-based access control for different stakeholder views
- Technologies: **JSP, Web Development, Interactive UI, Git Version Control**

<img src="{{ '/assets/img/projects/WoW/homepage_charts.png' | relative_url }}" alt='' width="900">
<img src="{{ '/assets/img/projects/WoW/char.png' | relative_url }}" alt='' width="900">  
<img src="{{ '/assets/img/projects/WoW/weapon.png' | relative_url }}" alt='' width="900">

<h2>Key Features</h2>
<h3>🎯 Character Data Management</h3>

- Comprehensive player profile tracking including levels, achievements, and inventory
- Real-time synchronization of game statistics
- Historical data tracking for player progression analysis

<h3>🔄 ETL Pipeline</h3>

- Automated data extraction from multiple game server logs
- Real-time and batch processing capabilities
- Data transformation for consistency across sources
- Quality checks and validation at each stage
- Error handling and recovery mechanisms

<h3>🛡️ Security Implementation</h3>
<ul>
<li>Prepared statements to prevent SQL injection</li>
<li>Input sanitization and validation at multiple layers</li>
<li>Secure session management and authentication</li>
<li>Encrypted sensitive data storage</li>
</ul>
<h3>📈 Analytics Engine</h3>

- Multi-dimensional analysis of player behavior
- Performance metrics and KPI tracking
- Custom report generation with export capabilities
- Trend analysis and predictive modeling support

<h3>👥 Stakeholder Portal</h3>

- Interactive data visualization with drill-down capabilities
- Real-time filtering and search functionality
- Responsive design for mobile and desktop access

<h2>Technical Architecture</h2>
The system follows a three-tier architecture:

- Presentation Layer: JSP pages with JSTL for dynamic content rendering
- Business Logic Layer: JAVA servlets handling request processing and business rules
- Data Access Layer: JDBC-based DAOs with connection pooling for efficient database access


<h2>Future Enhancements</h2>

- Migration to Spring Boot for improved scalability
- Implementation of RESTful APIs for mobile app integration
- Real-time data updates using WebSocket connections
- Machine learning integration for player behavior prediction


