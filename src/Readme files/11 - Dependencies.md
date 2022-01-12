## 1.11 - Dependencies 
Elaborate on dependencies in software, and how it’s related to the subject of the test.
***
### Dependencies between layers

***
### System resources

***
### Relations between objects

***
### Dependency inversion, Inversion of Control, Dependency Injection

***
### Mocks

Mocking is a process used in unit testing when the unit being tested has external dependencies.

The purpose of mocking is to isolate and focus on the code being tested and not on the behavior or state of external dependencies. In mocking, the dependencies are replaced by closely controlled replacements objects that simulate the behavior of the real ones.


There are three main possible types of replacement objects - **fakes, stubs and mocks**.

Example with hard-coded dependency

    public class DataTransformer {
    
        DataSource dataSource = new DBDataSource("some config");
    
        public int getSourceCount() {
            return dataSource.get().size();
        }
    }

Under normal circumstances the DataTransformer reads data from the DBDataSource, presumably from a database. Its function at the moment is simple: return the size of the data set. Since in this example the data source is instantiated explicitly, we have no means to replace it with a mock object for testing. We would like to be able to mock the DataSource nonetheless because we are testing DataTransformer only. Also, we are not interested in setting up a real environment from which a DBDataSource can read for us. We can solve this by injecting dependencies. Dependency injection can happen for example by passing the dependencies into a class via its constructor’s parameters.

Mock source

    public class DataSourceMock implements DataSource {
        @Override
        public List<Data> get() {
            return Arrays.asList(
        new Data("resolution", "fullhd"), new Data("memory", "16GB"));
        }
    }

Here we have a simple mock data source. We can modify the transformer so that it accepts the source.

Injected dependency

    public class DataTransformer {
    
        DataSource dataSource;
    
        public DataTransformer(DataSource dataSource) {
            this.dataSource = dataSource;
        }
    
        public int getSourceCount() {
            return dataSource.get().size();
        }
    }
This way our test can use the mock source above instead of having to fire up an actual data source connecting to a database.

    public class DataTransformerTest {
    
        DataTransformer dataTransformer;
    
        @Before
        public void setUp() {
            dataTransformer = new DataTransformer(new DBDataSourceMock());
    
        }
    
        @Test
        public void testSourceCount() {
            Assert.assertEquals(dataTransformer.getSourceCount(), 2);
        }
    }
