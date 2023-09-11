# ConfigurationAPI
## API for using yml in your projects.

### Usage
```java
public class ConfigManager {
    public YamlConfiguration config;
    private final File file;
    public ConfigManager() {
        file = new File("config.yml");
        config = YamlConfiguration.loadConfiguration(file);
    }

    public YamlConfiguration getConfig() {
        return config;
    }
    public void saveConfig() {
        try {
            config.save(file);
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
    }
}
```
