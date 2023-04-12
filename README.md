    package p.jaro.firstplugin.Listeners;

    import org.bukkit.ChatColor;
    import org.bukkit.entity.Player;
    import org.bukkit.event.EventHandler;
    import org.bukkit.event.Listener;
    import org.bukkit.event.player.AsyncPlayerChatEvent;

    public class ifOpListener implements Listener {
        @EventHandler
        public void onMessage(AsyncPlayerChatEvent event){
            Player player = (Player) event.getPlayer();
            String message = event.getMessage();
            if (player.isOp()){
                event.setFormat(ChatColor.RED+player.getName()+": "+ChatColor.GRAY+message);
            }
            else {
                event.setFormat(ChatColor.YELLOW+player.getName()+": "+ChatColor.GRAY+message);
            }
        }
    }
