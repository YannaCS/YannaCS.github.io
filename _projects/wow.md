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
<img src="{{ '/assets/img/projects/WoW/workflow.png' | relative_url }}" alt=''>

Watch how it works:
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

<img src="{{ '/assets/img/projects/WoW/ERD.jpg' | relative_url }}" alt=''>


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