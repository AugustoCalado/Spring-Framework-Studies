

## Selecting and Casting Object using EntityManager
```java
String sql = "SELECT USER.* FROM USER_ AS USER WHERE ID = ?";

Query query = em.createNativeQuery(sql, User.class);
query.setParameter(1, id);
User user = (User) query.getSingleResult();
```

## Get Next Value from Sequence with Spring 

### Using Repository
**OracleDB**
```java
public interface EventRepository extends JpaRepository<Event, Long> {

 @Query(value = "SELECT seq_name.nextval FROM dual", nativeQuery = 
        true)
 Long getNextSeriesId();
```

**PostgreeSQL**
```java
@Query(value = "SELECT nextval('item_id_seq')", nativeQuery =
            true)
    Long getNextSeriesId();
```

### Using Entity Manager
```java
@Autowired
EntityManager em;

Query q = em.createNativeQuery("select seq_name.nextval from dual");
return (Long)q.getSingleResult();
```



## Concurrency Control
[https://www.logicbig.com/tutorials/spring-framework/spring-data/pessimistic-locking-and-lock-annotation.html](https://www.logicbig.com/tutorials/spring-framework/spring-data/pessimistic-locking-and-lock-annotation.html)

## References

[StackOverflow - getting-next-value-from-sequence-with-spring-hibernate/46268483](https://stackoverflow.com/questions/46240529/getting-next-value-from-sequence-with-spring-hibernate/46268483)

postgree
[StackOverflow - getting-next-value-from-sequence-with-jpa-repository-in-postgresql](https://stackoverflow.com/questions/47490199/getting-next-value-from-sequence-with-jpa-repository-in-postgresql)
