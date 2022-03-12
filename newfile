class RegisterMemberHandler {
    private $members;

    public function __construct(MemberRepository $members) {
        $this->members = $members;
    }

    public function handle(RegisterMember $command) {
        $member = Member::register($command->email, $command->password);
        $this->members->save($member);
    }
}
