# KickIT: Football Scouting Database System

**A relational database system designed to centralize football (soccer) scouting operations, player tracking, transfer analysis, and talent identification using MySQL.**

## Overview

Football clubs track thousands of players across dozens of countries simultaneously, but scouting data is often scattered across spreadsheets, emails, and manual reports. Critical transfer decisions worth millions are frequently made with incomplete information. KickIT solves this by providing a centralized, normalized database system that supports complex queries for talent identification, maintains historical records for trend analysis, and ensures data integrity across interconnected entities.

## Database Design

The system uses a Class Table Inheritance (Supertype/Subtype) approach with 13+ primary entities and position-specific performance tables.

**Core Entities**: Player, Club, Scout, Performance, Transfer, Position, Country, League, Scout Report, Agent, National Team Appearances, Social Media, Market Value

**Position-Specific Performance Tables**: Separate tables for Attacker, Midfielder, Defender, and Goalkeeper performance metrics, each inheriting from a base Performance table. This allows position-relevant statistics (e.g., expected goals for attackers, tackles per 90 for defenders, save percentage for goalkeepers) to be tracked without null-heavy generic tables.

## Key Queries Implemented

1. **Multi-Position Versatility Report**: Identifies players who have performed well across three or more positions, useful for finding tactically flexible targets

2. **Emerging Talent vs. Established Player Comparison**: Compares young players (under 23) against established players (25+) in the same position and league using CTEs and conditional aggregation

3. **Undervalued Market Opportunities**: Surfaces high-performing players in lower-tier leagues with below-threshold market values, combining performance, market value, and social media data

4. **Scout Specialization Effectiveness**: Evaluates each scout's recommendation accuracy by tracking signing conversion rates and post-signing performance outcomes

5. **Global Marketability and Fanbase Reach Analysis**: Combines performance data with social media following, national team participation, and market value for commercial evaluation

6. **Agent Portfolio Performance and Negotiation Patterns**: Analyzes agent effectiveness by comparing client transfer fees against market averages using CTEs and cross joins

7. **Contract Expiration Opportunity Window**: Flags high-performing players with expiring contracts, estimating reduced transfer fees for acquisition planning

8. **Scout Coverage Gaps**: Identifies under-scouted countries and leagues containing quality talent, prioritized by scouting urgency level

## Technical Highlights

- Normalized relational design with proper foreign key constraints
- Class Table Inheritance for position-specific performance metrics
- Complex SQL queries using CTEs, window functions, conditional aggregation, and multi-table joins
- Indexed tables for query performance optimization
- Sample data population for demonstration and testing

## Tools and Technologies

- **Database**: MySQL
- **Design**: Entity-Relationship Diagram (ERD), forward engineering
- **Query Language**: SQL (advanced joins, subqueries, CTEs, aggregations)

## Lessons Learned

- Planning database structure early prevents confusion during implementation
- Clean and consistent data matters more than large volumes of data
- Complex queries become manageable once entity relationships are clearly defined
- Scope management is critical when working with many interconnected tables

## My Role

Designed and built the entire database system independently, including ERD design, table creation with constraints, sample data population, and all eight complex analytical queries.

## Contact

**Anugrah Suresh Kumar Nair**
- Email: anugrahsuresh12@gmail.com
- Phone: (857) 423-6265

*Northeastern University | Bouve College of Health Sciences | MS Health Informatics*
